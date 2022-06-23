# [OpenSeent](https://openseent-v1.web.app/)

A simple Ethereum-based decentralized application (dapp) for access to token-gated content. Based on the [ERC-721](https://erc721.org) standard, the OpenSeent NFT is minted by first being whitelisted, and then contributing sufficient funds via the [dapp](https://openseent.web.app/). A total of 0.3 testnet WETH (Wrapped Ether) are requested as a symbolic contribution to mint the NFT. Holding the NFT in an ethereum wallet serves as an identifier to access exclusive content. 

The current deployment on the Rinkeby test network is [here](https://rinkeby.etherscan.io/address/0x366818253baf43B6F0A9c64A10d2550af0986fA5). You must switch networks on Metamask to 'Rinkeby Test Network'. Faucet funds can be obtained [here](https://faucet.rinkeby.io/). The faucet will provide testnet ETH, that can be swapped on [Uniswap](https://uniswap.org) for 0.3 WETH. Verify the Rinkeby WETH token contract address is [0xc778417E063141139Fce010982780140Aa0cD5Ab](https://rinkeby.etherscan.io/address/0xc778417E063141139Fce010982780140Aa0cD5Ab). 

If you do not have Metamask Installed:

1. Download, install, and create Metamask wallet
2. Switch network to Rinkeby
2. Request Rinkeby faucet ETH
3. Swap Rinkeby ETH for WETH on Uniswap
4. Launch [OpenSeent](https://openseent.web.app/)

---

## Making Your Own Deployment

* **Node** - v14.x.x (preferrably v14.19.3 for long term support)
* **npm** - v6.x.x (preferrably v6.14.8)

## Built With

* [Truffle](https://www.trufflesuite.com/boxes/react) - Truffle React Box
* [Solidity](https://solidity.readthedocs.io/en/v0.5.3/) - Ethereum's smart contract programming language
* [React.js](https://reactjs.org/) - Javascript framework used
* [web3.js](https://github.com/ethereum/web3.js/) - Javascript library used to interact with the Ethereum blockchain
