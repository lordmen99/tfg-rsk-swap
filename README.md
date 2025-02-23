# Vue-RSK Swap Demo
 ### ![version](https://img.shields.io/badge/release-v1.0-blue.svg)

This project is the practical part of a Computer Engineering final degree project related to the RSK Blockchain. 

The goal of the project was to deploy two ERC20 tokens in the RSK Testnet Network and develop a dApp that replicates the basic functionalities of a DEX (Decentralized Exchange) such as Add Liquidity and Swap tokens. 


## ERC20 tokens

  - tokenA ($TKA) [0xD92084733Aca1149E6F36275Cd79083Fb34a1370](https://explorer.testnet.rsk.co/address/0xd92084733aca1149e6f36275cd79083fb34a1370)
  - tokenB ($TKB) [0x093060F7787D740C0185C402d5c1B1a7a427f858](https://explorer.testnet.rsk.co/address/0x093060f7787d740c0185c402d5c1b1a7a427f858)


## Liquidity Pools

To add liquidity of a token, the user will provide the balance of the token he wants to add along with the equivalent amount of RBTC, the RSK blockchain native token. 

Depending on whether the user wants to add liquidity of the tokenA ($TKA) or the tokenB ($TKB), will use the TokensA Liquidity Pool or the TokenB Liquidity Pool. 

The user will first indicate the amount of the token pool that he wants to contribute along with the amount of equivalent value of the RBTC token. This RBTC equivalent value is automatically calculated when the user inputs the token amount, based on the tokenX/RBTC price relation.  

It will then be necessary to approve the expenditure of these tokens through the Metamask wallet so the Smart Contract can spend the user tokens and finally confirm the liquidity aggregation transaction. 

![LiquidityPools](./public/img/LiquidityPools.PNG)

## Swap 

The Swap page provides the interface to exchanged between both ERC20 tokens deployed in RSK network. 

The user needs to select the input and output token, specify the amount of the input token he wants to exchange and the output token amount will be automatically calculated based on the price relation between both ERC20 tokens so the user don't have to manually calculate the output amount he will obtain. 

Like in the Liquidity provision process, the user will need to first approve the action, a needed process to give spending permissions to the Smart Contract. 

![Swap](./public/img/Swap.PNG)


# Router Contract

This Demo works with the Uniswap protocol UniswapV2Router02.sol, a Smart Contracts deployed both in the test and main RSK network. 

This contract is deployed at [0xf55c496bb1058690DB1401c4b9C19F3f44374961](https://explorer.testnet.rsk.co/address/0xf55c496bb1058690db1401c4b9c19f3f44374961) and provides functions to manage and maintain liquidity pools and exchange between tokens deployed in the RSK network. 

## Install Dependencies

```shell
npm install
```

## Run Development Environment

```shell
npm run dev
```

### App running at:
  - Local:   http://localhost:8080/
  - Network: http://192.168.1.70:8080/

## Stack
 ![Vue.js](https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vue.js&logoColor=4FC08D)
 ![Solidity](https://img.shields.io/badge/Solidity-007ACC?style=for-the-badge&logo=solidity&logoColor=white)
 ![JavaScript](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)

## Browser Support

<img src="https://s3.amazonaws.com/creativetim_bucket/github/browser/chrome.png" width="32" height="32"> <img src="https://s3.amazonaws.com/creativetim_bucket/github/browser/firefox.png" width="32" height="32"> <img src="https://s3.amazonaws.com/creativetim_bucket/github/browser/edge.png" width="32" height="32"> <img src="https://s3.amazonaws.com/creativetim_bucket/github/browser/safari.png" width="32" height="32"> <img src="https://s3.amazonaws.com/creativetim_bucket/github/browser/opera.png" width="32" height="32">



## Licensing

- Copyright 2018 Creative Tim (https://www.creative-tim.com/)

- Licensed under MIT (https://github.com/creativetimofficial/vue-black-dashboard/issues/blob/master/LICENSE.md)


