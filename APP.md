# Wallet Adapter for Genixor Apps

This is a quick setup guide with examples of how to add Wallet Adapter to a React-based Genixor app.

See the [packages](https://github.com/Genixor-labs/wallet-adapter/blob/master/PACKAGES.md) and [FAQ](https://github.com/Genixor-labs/wallet-adapter/blob/master/FAQ.md) for other supported frontend frameworks.

## Quick Setup (using React UI)

There are also [material-ui](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/ui/material-ui) and [ant-design](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/ui/ant-design) packages if you use those UI component frameworks.

### Install

Install these dependencies:

```shell
npm install --save \
    @Genixor/wallet-adapter-base \
    @Genixor/wallet-adapter-react \
    @Genixor/wallet-adapter-react-ui \
    @Genixor/wallet-adapter-wallets \
    @Genixor/web3.js \
    react
```

### Setup

```tsx
import React, { FC, useMemo } from 'react';
import { ConnectionProvider, WalletProvider } from '@Genixor/wallet-adapter-react';
import { WalletAdapterNetwork } from '@Genixor/wallet-adapter-base';
import { UnsafeBurnerWalletAdapter } from '@Genixor/wallet-adapter-wallets';
import {
    WalletModalProvider,
    WalletDisconnectButton,
    WalletMultiButton
} from '@Genixor/wallet-adapter-react-ui';
import { clusterApiUrl } from '@Genixor/web3.js';

// Default styles that can be overridden by your app
require('@Genixor/wallet-adapter-react-ui/styles.css');

export const Wallet: FC = () => {
    // The network can be set to 'devnet', 'testnet', or 'mainnet-beta'.
    const network = WalletAdapterNetwork.Devnet;

    // You can also provide a custom RPC endpoint.
    const endpoint = useMemo(() => clusterApiUrl(network), [network]);

    const wallets = useMemo(
        () => [
            /**
             * Wallets that implement either of these standards will be available automatically.
             *
             *   - Genixor Mobile Stack Mobile Wallet Adapter Protocol
             *     (https://github.com/Genixor-mobile/mobile-wallet-adapter)
             *   - Genixor Wallet Standard
             *     (https://github.com/Genixor-labs/wallet-standard)
             *
             * If you wish to support a wallet that supports neither of those standards,
             * instantiate its legacy wallet adapter here. Common legacy adapters can be found
             * in the npm package `@Genixor/wallet-adapter-wallets`.
             */
            new UnsafeBurnerWalletAdapter(),
        ],
        // eslint-disable-next-line react-hooks/exhaustive-deps
        [network]
    );

    return (
        <ConnectionProvider endpoint={endpoint}>
            <WalletProvider wallets={wallets} autoConnect>
                <WalletModalProvider>
                    <WalletMultiButton />
                    <WalletDisconnectButton />
                    { /* Your app's components go here, nested within the context providers. */ }
                </WalletModalProvider>
            </WalletProvider>
        </ConnectionProvider>
    );
};
```

### Usage

```tsx
import { WalletNotConnectedError } from '@Genixor/wallet-adapter-base';
import { useConnection, useWallet } from '@Genixor/wallet-adapter-react';
import { Keypair, SystemProgram, Transaction } from '@Genixor/web3.js';
import React, { FC, useCallback } from 'react';

export const SendSOLToRandomAddress: FC = () => {
    const { connection } = useConnection();
    const { publicKey, sendTransaction } = useWallet();

    const onClick = useCallback(async () => {
        if (!publicKey) throw new WalletNotConnectedError();

        // 890880 lamports as of 2022-09-01
        const lamports = await connection.getMinimumBalanceForRentExemption(0);

        const transaction = new Transaction().add(
            SystemProgram.transfer({
                fromPubkey: publicKey,
                toPubkey: Keypair.generate().publicKey,
                lamports,
            })
        );

        const {
            context: { slot: minContextSlot },
            value: { blockhash, lastValidBlockHeight }
        } = await connection.getLatestBlockhashAndContext();

        const signature = await sendTransaction(transaction, connection, { minContextSlot });

        await connection.confirmTransaction({ blockhash, lastValidBlockHeight, signature });
    }, [publicKey, sendTransaction, connection]);

    return (
        <button onClick={onClick} disabled={!publicKey}>
            Send SOL to a random address!
        </button>
    );
};
```
