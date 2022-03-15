# Virtual accounts

Tatum Virtual Accounts is a fully integrated suite of robust features ready to go on all supported blockchains within the platform. Virtual Accounts provide enhanced scalability features for legacy blockchains and represent a parallel layer of advanced functionality that is seamlessly integrated with native blockchain operations in Tatum.

- [Setup for BTC,LTC,DOGE,BCH](https://docs.tatum.io/guides/ledger-and-off-chain/how-to-set-up-virtual-accounts-with-btc-ltc-doge-and-bch)
- [Setup for XRP, BNB, XLM](https://docs.tatum.io/guides/ledger-and-off-chain/how-to-set-up-virtual-accounts-with-xrp-bnb-and-xlm)
- [Setup for ETH, TRON, CELO, MATIC, ONE](https://docs.tatum.io/guides/ledger-and-off-chain/how-to-set-up-virtual-accounts-with-eth-tron-celo-matic-bsc-and-one)
- [Send feeless instant transactions](https://docs.tatum.io/guides/ledger-and-off-chain/how-to-send-feeless-instant-transaction)
- [Send Bitcoin transaction from Virtual account](https://docs.tatum.io/guides/ledger-and-off-chain/how-to-send-blockchain-transaction-from-the-ledger-account)
- [Block amounts in Virtual account](https://docs.tatum.io/guides/ledger-and-off-chain/how-to-block-amounts-on-the-account)
- [Create custom Virtual currency](https://docs.tatum.io/guides/ledger-and-off-chain/how-to-support-fiat-currencies)
- [Connect custom ERC-20 to a Virtual account](https://docs.tatum.io/guides/ledger-and-off-chain/how-to-connect-custom-erc-20-token-to-the-ledger)
- [Withdraw assets from Virtual aacounts with gas pump wallets](https://docs.tatum.io/guides/ledger-and-off-chain/how-to-withdraw-assets-from-ledger-accounts-with-custodial-wallets)

## Create virtual account
 It is possible to create an account for every supported cryptocurrency, FIAT, any ERC20 token created within a Tatum instance, and Tatum virtual currencies. When the customer field is already present, the account is added to the customer's list of accounts. If the customer field is not present, a new customer is created along with the account.

Every account has its own balance. Tatum supports 2 types of balances 
- `accountBalance` = All assets in the account (available and blocked)
- `availableBalance` = `accountBalance` - `blockedAmount` in the account. Determine how much a customer can send or withdraw from the account.


### Virtual account currencies
An account is always created with a specific currency. Once the currency is set, it cannot be changed.

#### Extended public key - xpub
When an account's currency is blockchain-based, like BTC or ETH, the account is usually created with xpub. Xpub represents an extended public key of the blockchain wallet, which will be connected to this account. Adding xpub to the account does not connect any specific blockchain address to this account. Xpub is just a generator of addresses, not an address itself.

Every blockchain has different types of xpubs:

Chain| xpub source | other supported currencies
---------|----------|----------
 ADA | [AdaGenerateWallet](https://docs.tatum.io/rest/blockchain/generate-cardano-wallet) | 
 ALGO | [AlgoGenerateWallet](https://docs.tatum.io/rest/blockchain/generate-algorand-wallet) | 
 BCH | [BchGenerateWallet](https://docs.tatum.io/rest/blockchain/generate-bitcoin-cash-wallet)|  
 BNB | [BnbGenerateWallet](https://docs.tatum.io/rest/blockchain/generate-binance-wallet) | 
 BSC | [BscGenerateWallet](https://docs.tatum.io/rest/blockchain/generate-bsc-wallet)| GMC_BSC, CAKE, BUSD_BSC, BBTC, BETH, BADA, BBNB, BDOT, BXRP, BLTC, BBCH, RMB, USDC_BSC
 BTC | [BtcGenerateWallet](https://docs.tatum.io/rest/blockchain/generate-btc-wallet) | 
 CELO, | [CeloGenerateWallet](https://docs.tatum.io/rest/blockchain/generate-celo-wallet) | cEUR, cUSD
 DOGE | [DogeGenerateWallet](https://docs.tatum.io/rest/blockchain/generate-dogecoin-wallet) | 
 EGLD | [EgldGenerateWallet](https://docs.tatum.io/rest/blockchain/generate-elrond-wallet) | 
 ETH/ERC20 | [EthGenerateWallet](https://docs.tatum.io/rest/blockchain/generate-ethereum-wallet) |  GMC, ERC20, SAND, REVV, PLTC, BUSD, BAT, LATOKEN, USDT, WBTC, USDC, TUSD, MKR, LINK, PAX, PAXG, UNI, LEO, FREE, XCON
 FLOW | [GenerateFlowwallet](https://docs.tatum.io/rest/blockchain/generate-flow-wallet)| FUSD
 KCS| [KcsGenerateWallet](https://docs.tatum.io/rest/blockchain/generate-kucoin-wallet)| 
 KLAY | [KlaytnGenerateWallet](https://docs.tatum.io/rest/blockchain/generate-klaytn-wallet) | 
 MATIC | [PolygonGenerateWallet](https://docs.tatum.io/rest/blockchain/generate-matic-wallet) | MATIC_ETH, USDT_MATIC, GAMEE, USDC_MATIC
 NEO | [NeonGenerateWallet](https://docs.tatum.io/rest/blockchain/generate-neo-wallet) | GAS
 LTC | [LtcGenerateWallet](https://docs.tatum.io/rest/blockchain/generate-litecoin-wallet) | 
 SOL | [SolanaGenerateWallet](https://docs.tatum.io/rest/blockchain/generate-solana-wallet) | 
 TRON and TRC tokens | [GenerateTronwallet](https://docs.tatum.io/rest/blockchain/generate-tron-wallet) | USDT_TRON, INRT_TRON
 XDC | [XdcGenerateWallet](https://docs.tatum.io/rest/blockchain/generate-xdc-wallet) | 





