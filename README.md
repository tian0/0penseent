# OpenSeent

A simple Ethereum-based decentralized application (dapp) for token-gated access to content enabled for token holders. Based on the [ERC-721](https://erc721.org) standard, the OpenSeent NFT is minted by first being whitelisted, and then contributing sufficient funds via the [dapp](https://openseent.web.app/). A total of 0.3 testnet WETH (Wrapped Ether) are requested as a symbolic contribution to mint the NFT. Holding the NFT in an ethereum wallet serves as an identifier to access exclusive content. 

The current deployment is on the Rinkeby test network. You must switch networks on Metamask to Rinkeby. Faucet funds for Rinkeby can be obtained [here](https://faucet.rinkeby.io/). The faucet will provide testnet ETH, that can be swapped on [Uniswap](https://uniswap.org) for 0.3 WETH. Verify the Rinkeby WETH token contract address is [0xc778417E063141139Fce010982780140Aa0cD5Ab](https://rinkeby.etherscan.io/address/0xc778417E063141139Fce010982780140Aa0cD5Ab). 

If you do not have Metamask Installed:

1. Download, install, and create Metamask wallet
2. Switch network to Rinkeby
2. Request Rinkeby faucet ETH
3. Swap Rinkeby ETH for WETH on Uniswap
4. Launch [OpenSeent](https://openseent.web.app/)

---

## Prerequisites

* **Node** - v14.x.x (preferrably v14.19.3 for long term support)
* **npm** - v6.x.x (preferrably v6.14.8)

## Making Your Own Deployment

Clone this repo to your local machine and install the dependencies as follows:

```bash
git clone https://github.com/tian0/openseent.git
cd openseent
yarn install
```

A contract deployment instance is available on Ethereum's Rinkeby testnet, at the following address: 
`0x366818253baf43B6F0A9c64A10d2550af0986fA5`

To deploy your own contract instance on Rinkeby, first paste your own INFURA_PROJECT_ID and contract owner wallet MNEMONIC in the .env file, and in the terminal run:
```bash
truffle compile
truffle migrate --network rinkeby
```

To deploy locally, first install and run an Ethereum development testnet using [Ganache](https://www.trufflesuite.com/ganache):

```bash
npm install -g ganache-cli
ganache-cli
```

After ganache launches, run the following to compile and deploy the Membership contract:

```bash
truffle compile
truffle migrate
```

Finally, install the client dependencies and serve the application in the development environment via:

```bash
cd client
yarn install
yarn start
```

There are 4 dashboards: 

**Non-whitelisted:**
Must contact contract owner to become whitelisted via kyc process to interact with contract

**Whitelisted non-member:**
Only whitelisted addresses will be able to have the NFT minted to their address to become members. Whitelisted non-members must [Approve-WETH] and [Send-Contribution] to become members. 

**Member:**
Will be able to see the contract details and have access to exclusive content provided by the contract owner on their dashboard. The NFT will serve as the member's wallet identifier forever.

**Owner:**
Can withdraw the reserve currency balance by clicking the [Withdraw-Reserves] button. Owners can whitelist addresses by pasting one or several comma-separated addresses in the Member Management section and clicking the [Whitelist] button. The Contract Management Panel allows the owner to [Pause], [Unpause], and [Kill] the contract.

## Built With

* [Truffle](https://www.trufflesuite.com/boxes/react) - Truffle React Box
* [Solidity](https://solidity.readthedocs.io/en/v0.5.3/) - Ethereum's smart contract programming language
* [React.js](https://reactjs.org/) - Javascript framework used
* [web3.js](https://github.com/ethereum/web3.js/) - Javascript library used to interact with the Ethereum blockchain
