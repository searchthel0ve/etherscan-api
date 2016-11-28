# Etherscan API

[![npm version](https://badge.fury.io/js/etherscan-api.svg)](https://badge.fury.io/js/etherscan-api) [![Build Status](https://travis-ci.org/sebs/etherscan-api.svg?branch=master)](https://travis-ci.org/sebs/etherscan-api) [![npm](https://img.shields.io/npm/dt/etherscan-api.svg?maxAge=2592000)]()

A way to access the [etherscan.io api](https://etherscan.io/apis) using promises. Fetch a diverse set of information about the blockchain


```javascript
var api = require('etherscan-api').init('KMK786MB5AZYQSFS5CW3JQ9AAW4DCX3AX4');
var balance = api.account.balance('0xbb9bc244d798123fde783fcc1c72d3bb8c189413');
balance.then(function(balanceData){
  console.log(balanceData);
});
```

 ## Install

 ```bash
 npm install etherscan-api --save
 ```
## Api

[Full Api Docs](https://sebs.github.io/etherscan-api/)

* block.getblockreward
* transaction.getstatus
* contract.getabi
* account
  * getminedblocks
  * tokenbalance by name
  * tokenbalance by address
  * txlist
  * txlistinternal
  * balance
  * balance multi
* stats
  * ethsupply
  * tokensupply by tokenname
  * tokensupply by address
  * ethprice
* proxy
  * proxy.eth_blockNumber
  * proxy.eth_getBlockByNumber
  * proxy.eth_getUncleByBlockNumberAndIndex
  * proxy.eth_getBlockTransactionCountByNumber
  * proxy.eth_getTransactionByHash
  * proxy.eth_getTransactionByBlockNumberAndIndex
  * proxy.eth_getTransactionCount
  * proxy.eth_sendRawTransaction
  * proxy.eth_getTransactionReceipt
  * proxy.eth_call
  * proxy.eth_getCode
  * proxy.eth_getStorageAt
  * proxy.eth_gasPrice
  * proxy.eth_estimateGas
