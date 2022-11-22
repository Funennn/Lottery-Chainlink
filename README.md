# ♤ Lottery ♤
> Lottery
> Contract inspired by ILESKOV was used VRFv2 for generating random numbers. Therefore, for the correct operation of the contract, it is necessary to create subscription on 
> https://vrf.chain.link/goerli for rinkeby testnet or https://vrf.chain.link/mainnet for [mainnet], replenish the balance of LINK and add contract address as a consumer

## Table of Contents
* [General Info](general-information)
* [Technologies Used](technologies-used)
* [Features](features)
* [Requirements](requirements)
* [Setup](setup)
* [Contact](contact)


## General Information
- Owner(admin) of the contract can start/end lottery
- Owner(admin) can pause the contract 
- Every user can participate and price of ticket is based on TICK ERC20 tokens. Each ticket represents itself an ERC721 token
- After owner end lottery, the winner will be picked using randomness from Chainlink VRFv2 Coordinator
 
## Technologies Used
- Chainlink VRFv2
- hh coverage
- slither
- docgen

## Features
- Contract can be randome
- Ticket price is based TICK tokens
- The contract has been optimized.

## Requirements
- Install [NodeJS](https://nodejs.org/en/), should work with any node version below 16.16.0
- Install [Hardhat](https://hardhat.org/)

## Setup
### 1. Clone / Download the Repository
### 2. Install Dependencies :

```
$ cd lottery_file
$ npm install
```

### 3. Setup .env environment variables required

You need to Create `.env` file inside project folder

- You can get your ethereum or testnet API key [here](https://infura.io/dashboard/ethereum),[here](https://www.alchemy.com) or any other service that allow you to connect to the nodes
- You can get your private key from your wallet (Don't share your private key with untrusted parties) 
- Subscription id can be obtained here after creation of subscription [here](https://vrf.chain.link)
- Key Hash and address of vrf coordinator can be obtained from here [here](https://docs.chain.link/docs/vrf-contracts) Just choose network and copy:)
- You can get your etherscan API -key [here](https://etherscan.io/myapikey).
- LOT_ADDRESS be available after deploying contracts
```
GOERLI_API = <Goerli API key>
MAINNET_API = <Ethereum mainnet API key>
PRIVATE_KEY = <Private key of your wallet u want to deploy contracts from>
ETHERSCAN_KEY = <Etherscan API key in order to verify your contracts>
SUBSCRIPTION_ID = <VRFv2 subcription id>
KEY_HASH = <Key Hash>
AGGREGATOR = <Aggregator address(depends on network)>
VRF_COORDINATOR = <VRF coordinator address(depends on network)>
PERCENT_WINNER = <Percent of total collected funds of lottery winner will receive(PERCENT_WINNER+PERCENT_OWNER must be 100)>
PERCENT_OWNER = <Percent of total collected funds of lottery winner will receive(PERCENT_WINNER+PERCENT_OWNER must be 100)>
TICKET_PRICE = <Price in LOT tokens in order to participate in Lottery>
```
<!--![Example screenshot](./helpers/Screenshot8.png)-->

### 4. ⚠️ Run Tests
```
$ npm run test
```

```
$ npm run coverage
```

### 5. 🚀 Deploy to GORELI testnet or Mainnet
```
$ npm run deploy:goerli
``` 
```
$ npm run deploy:polygon
``` 
```
$ npm run deploy:mainnet
``` 
### Note:
deploy.ts implements the verification script and you don't need to complete any additional steps in order to verify the contract.


## Contact
contact me - [Vanen](https://www.linkedin.com/in/vanen-surya-04511717b/)
