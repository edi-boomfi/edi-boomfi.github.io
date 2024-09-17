# BoomFi Crypto Payments for WooCommerce

## Overview

`BoomFi Crypto Payments for WooCommerce` is a crypto payment plugin for WooCommerce. With BoomFi Crypto Payments, you can accept payments 
via major cryptocurrencies such as USDC, USDT, DAI, WETH, ETH over multiple networks such as Polygon, Arbitrium, 
Ethereum, Tron, Solana, Binance Smart Chain and Base.

**Supported Networks and Crypto Currencies**

| Technology | Network                                                            | Currencies                                                                                                                                                                                                                                                                                                                            |
|------------|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EVM        | [Polygon](https://polygon.technology/polygon-pos)                  | [USDC](https://polygonscan.com/token/0x3c499c542cef5e3811e1192ce70d8cc03d5c3359), [USDT](https://polygonscan.com/token/0xc2132d05d31c914a87c6611c10748aeb04b58e8f), [DAI](https://polygonscan.com/token/0x8f3cf7ad23cd3cadbd9735aff958023239c6a063), [WETH](https://polygonscan.com/token/0x7ceb23fd6bc0add59e62ac25578270cff1b9f619) |
| EVM        | [Arbitrium One](https://arbitrum.io/)                              | [USDC](https://arbiscan.io/token/0xaf88d065e77c8cc2239327c5edb3a432268e5831), [USDT](https://arbiscan.io/token/0xfd086bc7cd5c481dcc9c85ebe478a1c0b69fcbb9), [DAI](https://arbiscan.io/token/0xda10009cbd5d07dd0cecc66161fc93d7c9000da1), [WETH](https://arbiscan.io/token/0x82af49447d8a07e3bd95bd0d56f35241523fbab1)                 |
| EVM        | [Ethereum](https://ethereum.org/en/)                               | [USDC](https://etherscan.io/token/0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48), [USDT](https://etherscan.io/token/0xdac17f958d2ee523a2206206994597c13d831ec7), [DAI](https://etherscan.io/token/0x6b175474e89094c44da98b954eedeac495271d0f), [WETH](https://etherscan.io/token/0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2), ETH        |
| EVM        | [Binance Smart Chain](https://www.bnbchain.org/en/bnb-smart-chain) | [USDC](https://bscscan.com/token/0x8ac76a51cc950d9822d68b83fe1ad97b32cd580d), [USDT](https://bscscan.com/token/0x55d398326f99059fF775485246999027B3197955), [DAI](https://bscscan.com/token/0x1AF3F329e8BE154074D8769D1FFa4eE058B1DBc3), [WETH](https://bscscan.com/token/0x4DB5a66E937A9F4473fA95b1cAF1d1E1D62E29EA)                 |
| EVM        | [Base](https://www.base.org/)                                      | [USDC](https://basescan.org/token/0x833589fcd6edb6e08f4c7c32d4f71b54bda02913), [DAI](https://basescan.org/token/0x50c5725949A6F0c72E6C4a641F24049A917DB0Cb), [WETH](https://basescan.org/token/0x4200000000000000000000000000000000000006), ETH                                                                                       |                                                                                                                 
| Tron       | [Tron](https://tron.network/)                                      | [USDC](https://tronscan.io/#/token20/TEkxiTehnzSmSe2XqrBj4w32RUN966rdz8), [USDT](https://tronscan.io/#/token20/TR7NHqjeKQxGTCi8q8ZY4pL8otSzgjLj6t)                                                                                                                                                                                    |                                                                                                        
| Solana     | [Solana](https://solana.com/)                                      | [USDC](https://solscan.io/token/EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v)                                                                                                                                                                                                                                                         |

## Third Party Access

The plugin will access the BoomFi Merchant API (https://mapi.boomfi.xyz) to process the payment.
To use the plugin, the merchant has to obtain an API Key and payment link from the BoomFi Merchant portal (https://app.boomfi.xyz) after completing the signup process.
The user who checked out the payment using the plugin will be able to see past transactions via the BoomFi customer portal (https://customer.boomfi.xyz/customer/login).

| Mode | Merchant API                 | Merchant Portal         | Customer Portal                  |
|------|------------------------------|-------------------------|----------------------------------|
| Test | https://mapi-test.boomfi.xyz | https://test.boomfi.xyz | https://customer-test.boomfi.xyz |
| Live | https://mapi.boomfi.xyz      | https://app.boomfi.xyz  | https://customer.bomfi.xyz       |

## Data Collection

BoomFi Crypto Payments for WooCommerce plugin records the following information

| Domain   | Information       | Purpose                                                           |
|----------|-------------------|-------------------------------------------------------------------|
| Merchant | email address     | Merchant portal authentication, onboarding and email notification |
| Merchant | username          | onboarding process                                                |                                                               
| Merchant | organization name | onboarding process                                                |                                               
| Merchant | wallet address    | Settle collected payments to merchant wallet                      |
| Customer | email address     | Customer portal authentication and email notification             |
| Customer | wallet address    | Transaction history and refund processing                         |

You may refer to BoomFi terms and conditions at [https://www.boomfi.xyz/legal-pages](https://www.boomfi.xyz/legal-pages).

## Prerequisites
1. WordPress hosting to host the woocommerce based eCommerce
2. Install, enable and configure [WooCommerce](https://wordpress.org/plugins/woocommerce/) plugin
3. Wallet accounts
   1. EVM based blockchain accounts (Polygon, Arbitrium One, Ethereum, Binance Smart Chain, Base) using [Metamask](https://metamask.io/download/) or something similar. Add EVM based networks (Polygon, Arbitrium One, Ethereum, Binance Smart Chain, and Base) and import the tokens (USDC, USDT, DAI and WETH)
   2. Tron wallet account [TronLink](https://www.tronlink.org/), or something similar
   3. Solana wallet account [Phantom](https://phantom.app/en-GB), or something similar
4. An account at BoomFi, signup at ([Test](https://test.boomfi.xyz/signup), [Live](https://app.boomfi.xyz/signup)) and complete KYB process

## How to test the plugin

We will be using BoomFi Crypto payments in test mode using simulated payment. Since the payment is simulated there will be no amount of cryptocurrency collected from customer wallet and no amount of cryptocurrency transferred to merchant wallet.

The tutorial consists of four parts
1. [Installing and configuring MetaMask](01-installing-and-configuring-metamask.md)
2. [Signing up and configuring BoomFi merchant account](02-signing-up-and-configuring-boomfi-merchant-account.md)
3. [Installing and configuring BoomFi Crypto Payments for WooCommerce plugin](03-installing-and-configuring-boomfi-crypto-payments-plugin.md)
4. [Payment testing](04-payment-testing.md)

## How to Configure Plugin In Live Environment

To configure the plugin in the live environment

1. You can reuse the wallet address from [first tutorial](01-installing-and-configuring-metamask.md)
2. Sign up to [BoomFi Live](https://app.boomfi.xyz) environment and complete KYB
3. Configure settlement account, create payment link and create an API key. All the steps are exactly the same as the [second tutorial](02-signing-up-and-configuring-boomfi-merchant-account.md) except that it's using live environment
4. Similar to [third tutorial](03-installing-and-configuring-boomfi-crypto-payments-plugin.md), change the environment to Live, paste API key and payment link and "Save Changes"