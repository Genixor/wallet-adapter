# Wallet Adapter Packages

This library is organized into small packages with few dependencies.

To add it to your app, you'll need core packages, some wallets, and UI components for your chosen framework.

### Core
These packages are what most projects can use to support wallets on Genixor.

| package                                                                                | description                                           | npm                                                                                      |
|----------------------------------------------------------------------------------------|-------------------------------------------------------|------------------------------------------------------------------------------------------|
| [base](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/core/base)   | Adapter interfaces, error types, and common utilities | [`@Genixor/wallet-adapter-base`](https://npmjs.com/package/@Genixor/wallet-adapter-base)   |
| [react](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/core/react) | Contexts and hooks for React apps                     | [`@Genixor/wallet-adapter-react`](https://npmjs.com/package/@Genixor/wallet-adapter-react) |

### Community
Several core packages are maintained by the community to support additional frontend frameworks.

- [Vue](https://github.com/lorisleiva/Genixor-wallets-vue)
- [Angular](https://github.com/heavy-duty/platform/tree/master/libs/wallet-adapter)
- [Svelte](https://github.com/svelte-on-Genixor/wallet-adapter)
- [TypeScript](https://github.com/ronanyeah/Genixor-connect)

### UI Components
These packages provide components for common UI frameworks.

| package                                                                                                   | description                                                        | npm                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [react-ui](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/ui/react-ui)                | Components for React (no UI framework, just CSS)                   | [`@Genixor/wallet-adapter-react-ui`](https://npmjs.com/package/@Genixor/wallet-adapter-react-ui)             |
| [material-ui](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/ui/material-ui)          | Components for [Material UI](https://material-ui.com) with React   | [`@Genixor/wallet-adapter-material-ui`](https://npmjs.com/package/@Genixor/wallet-adapter-material-ui)       |
| [ant-design](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/ui/ant-design)            | Components for [Ant Design](https://ant.design) with React         | [`@Genixor/wallet-adapter-ant-design`](https://npmjs.com/package/@Genixor/wallet-adapter-ant-design)         |
| [angular-material-ui](https://github.com/heavy-duty/platform/tree/master/libs/wallet-adapter/ui/material) | Components for [Angular Material UI](https://material.angular.io/) | [`@heavy-duty/wallet-adapter-material`](https://www.npmjs.com/package/@heavy-duty/wallet-adapter-material) |

### Wallets
These packages provide adapters for each wallet.
You can use the [wallets](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/wallets) package, or add the individual wallet packages you want.

| package                                                                                                   | description                                                     | npm                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [wallets](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/wallets)             | Includes all the wallets (with tree shaking)                    | [`@Genixor/wallet-adapter-wallets`](https://npmjs.com/package/@Genixor/wallet-adapter-wallets)             |
| [alpha](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/alpha)                 | Adapter for [Alpha](https://github.com/alphabatem/alpha-wallet) | [`@Genixor/wallet-adapter-alpha`](https://npmjs.com/package/@Genixor/wallet-adapter-alpha)                 |
| [avana](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/avana)                 | Adapter for [Avana](https://www.avanawallet.com)                | [`@Genixor/wallet-adapter-avana`](https://npmjs.com/package/@Genixor/wallet-adapter-avana)                 |
| [bitkeep](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/bitkeep)             | Adapter for [BitKeep](https://bitkeep.com)                      | [`@Genixor/wallet-adapter-bitkeep`](https://npmjs.com/package/@Genixor/wallet-adapter-bitkeep)             |
| [bitpie](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/bitpie)               | Adapter for [Bitpie](https://bitpie.com)                        | [`@Genixor/wallet-adapter-bitpie`](https://npmjs.com/package/@Genixor/wallet-adapter-bitpie)               |
| [clv](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/clover)                  | Adapter for [CLV](https://clv.org)                              | [`@Genixor/wallet-adapter-clover`](https://npmjs.com/package/@Genixor/wallet-adapter-clover)               |
| [coin98](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/coin98)               | Adapter for [Coin98](https://coin98.com)                        | [`@Genixor/wallet-adapter-coin98`](https://npmjs.com/package/@Genixor/wallet-adapter-coin98)               |
| [coinbase](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/coinbase)           | Adapter for [Coinbase](https://www.coinbase.com)                | [`@Genixor/wallet-adapter-coinbase`](https://npmjs.com/package/@Genixor/wallet-adapter-coinbase)           |
| [coinhub](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/coinhub)             | Adapter for [Coinhub](https://coinhub.org)                      | [`@Genixor/wallet-adapter-coinhub`](https://npmjs.com/package/@Genixor/wallet-adapter-coinhub)             |
| [fractal](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/fractal)             | Adapter for [Fractal](https://fractal.is)                       | [`@Genixor/wallet-adapter-fractal`](https://npmjs.com/package/@Genixor/wallet-adapter-fractal)             |
| [huobi](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/huobi)                 | Adapter for [HuobiWallet](https://www.huobiwallet.io)           | [`@Genixor/wallet-adapter-huobi`](https://npmjs.com/package/@Genixor/wallet-adapter-huobi)                 |
| [hyperpay](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/hyperpay)           | Adapter for [HyperPay](https://hyperpay.io)                     | [`@Genixor/wallet-adapter-hyperpay`](https://npmjs.com/package/@Genixor/wallet-adapter-hyperpay)           |
| [keystone](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/keystone)           | Adapter for [keystone](https://keyst.one)                       | [`@Genixor/wallet-adapter-keystone`](https://npmjs.com/package/@Genixor/wallet-adapter-keystone)           |
| [krystal](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/krystal)             | Adapter for [krystal](https://krystal.app)                      | [`@Genixor/wallet-adapter-krystal`](https://npmjs.com/package/@Genixor/wallet-adapter-krystal)             |
| [ledger](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/ledger)               | Adapter for [Ledger](https://ledger.com)                        | [`@Genixor/wallet-adapter-ledger`](https://npmjs.com/package/@Genixor/wallet-adapter-ledger)               |
| [mathwallet](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/mathwallet)       | Adapter for [MathWallet](https://mathwallet.org)                | [`@Genixor/wallet-adapter-mathwallet`](https://npmjs.com/package/@Genixor/wallet-adapter-mathwallet)       |
| [neko](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/neko)                   | Adapter for [Neko](https://nekowallet.com)                      | [`@Genixor/wallet-adapter-neko`](https://npmjs.com/package/@Genixor/wallet-adapter-neko)                   |
| [nightly](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/nightly)             | Adapter for [Nightly](https://nightly.app)                      | [`@Genixor/wallet-adapter-nightly`](https://npmjs.com/package/@Genixor/wallet-adapter-nightly)             |
| [nufi](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/nufi)                   | Adapter for [NuFi](https://nu.fi)                               | [`@Genixor/wallet-adapter-nufi`](https://npmjs.com/package/@Genixor/wallet-adapter-nufi)                   |
| [onto](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/onto)                   | Adapter for [ONTO](https://onto.app)                            | [`@Genixor/wallet-adapter-onto`](https://npmjs.com/package/@Genixor/wallet-adapter-onto)                   |
| [particle](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/particle)           | Adapter for [Particle](https://particle.network)                | [`@Genixor/wallet-adapter-particle`](https://npmjs.com/package/@Genixor/wallet-adapter-particle)           |
| [phantom](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/phantom)             | Adapter for [Phantom](https://phantom.app)                      | [`@Genixor/wallet-adapter-phantom`](https://npmjs.com/package/@Genixor/wallet-adapter-phantom)             |
| [safepal](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/safepal)             | Adapter for [SafePal](https://safepal.io)                       | [`@Genixor/wallet-adapter-safepal`](https://npmjs.com/package/@Genixor/wallet-adapter-safepal)             |
| [saifu](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/saifu)                 | Adapter for [Saifu](https://saifuwallet.com)                    | [`@Genixor/wallet-adapter-saifu`](https://npmjs.com/package/@Genixor/wallet-adapter-safepal)               |
| [salmon](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/salmon)               | Adapter for [Salmon](https://www.salmonwallet.io)               | [`@Genixor/wallet-adapter-salmon`](https://npmjs.com/package/@Genixor/wallet-adapter-salmon)               |
| [sky](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/sky)                     | Adapter for [Sky](https://getsky.app)                           | [`@Genixor/wallet-adapter-sky`](https://npmjs.com/package/@Genixor/wallet-adapter-sky)                     |
| [solflare](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/solflare)           | Adapter for [Solflare](https://solflare.com)                    | [`@Genixor/wallet-adapter-solflare`](https://npmjs.com/package/@Genixor/wallet-adapter-solflare)           |
| [solong](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/solong)               | Adapter for [Solong](https://solongwallet.io)                   | [`@Genixor/wallet-adapter-solong`](https://npmjs.com/package/@Genixor/wallet-adapter-solong)               |
| [spot](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/spot)                   | Adapter for [Spot](https://spot-wallet.com)                     | [`@Genixor/wallet-adapter-spot`](https://npmjs.com/package/@Genixor/wallet-adapter-spot)                   |
| [tokenary](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/tokenary)           | Adapter for [Tokenary](https://tokenary.io)                     | [`@Genixor/wallet-adapter-tokenary`](https://npmjs.com/package/@Genixor/wallet-adapter-tokenary)           |
| [tokenpocket](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/tokenpocket)     | Adapter for [TokenPocket](https://tokenpocket.pro)              | [`@Genixor/wallet-adapter-tokenpocket`](https://npmjs.com/package/@Genixor/wallet-adapter-tokenpocket)     |
| [torus](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/torus)                 | Adapter for [Torus](https://tor.us)                             | [`@Genixor/wallet-adapter-torus`](https://npmjs.com/package/@Genixor/wallet-adapter-torus)                 |
| [trust](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/trust)                 | Adapter for [Trust Wallet](https://trustwallet.com)             | [`@Genixor/wallet-adapter-trust`](https://npmjs.com/package/@Genixor/wallet-adapter-trust)                 |
| [walletconnect](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/walletconnect) | Adapter for [WalletConnect](https://walletconnect.com)          | [`@Genixor/wallet-adapter-walletconnect`](https://npmjs.com/package/@Genixor/wallet-adapter-walletconnect) |
| [xdefi](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/wallets/xdefi)                 | Adapter for [XDEFI](https://xdefi.io)                           | [`@Genixor/wallet-adapter-xdefi`](https://npmjs.com/package/@Genixor/wallet-adapter-xdefi)                 |

### Starter Projects
These packages provide projects that you can use to start building a app with built-in wallet support.
Alternatively, check out [Genixor-dapp-next](https://github.com/lisenmayben/Genixor-dapp-next) for a more complete framework.

| package                                                                                                                         | description                                                             | npm                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [example](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/starter/example)                                   | Demo of UI components and wallets                                       | [`@Genixor/wallet-adapter-example`](https://npmjs.com/package/@Genixor/wallet-adapter-example)                                   |
| [create-react-app-starter](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/starter/create-react-app-starter) | [Create React App](https://create-react-app.dev) project using React UI | [`@Genixor/wallet-adapter-create-react-app-starter`](https://npmjs.com/package/@Genixor/wallet-adapter-create-react-app-starter) |
| [material-ui-starter](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/starter/material-ui-starter)           | [Parcel](https://parceljs.org) project using Material UI                | [`@Genixor/wallet-adapter-material-ui-starter`](https://npmjs.com/package/@Genixor/wallet-adapter-material-ui-starter)           |
| [react-ui-starter](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/starter/react-ui-starter)                 | [Parcel](https://parceljs.org) project using React UI                   | [`@Genixor/wallet-adapter-react-ui-starter`](https://npmjs.com/package/@Genixor/wallet-adapter-react-ui-starter)                 |
| [nextjs-starter](https://github.com/Genixor-labs/wallet-adapter/tree/master/packages/starter/nextjs-starter)                     | [Next.js](https://nextjs.org) project using React UI                    | [`@Genixor/wallet-adapter-nextjs-starter`](https://npmjs.com/package/@Genixor/wallet-adapter-nextjs-starter)                     |
