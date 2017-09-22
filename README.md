# Bitcoin Cash JSON-RPC library

## Javascript Library to communicate with your Bitcoin Unlimited / Bitcoin ABC / Bitcoin Classic Node.


![header](https://cloud.githubusercontent.com/assets/.png)

This is a promise-based library and async/await compatible.

## Installation

grab from NPM
```
    npm i bitcoin-cash-rpc
```

## Usage

```
let BCC = require("./BitcoinCashRPC");
let bcc = new BCC(host, username, password, port, 3000);

```


```
 let info = await bcc.getInfo();
 //console.log(info)
 // results in
 //{
 //  "version": 1010101,
 //  "protocolversion": 80003,
 //  "walletversion": 60000,
 //  "balance": 0.00000000,
 //  "blocks": 478559,
 //  "timeoffset": 0,
 //  "connections": 12,
 //  "proxy": "",
 //  "difficulty": 29829733124.04042,
 //  "testnet": false,
 //  "keypoololdest": 1506057198,
 //  "keypoolsize": 100,
 //  "paytxfee": 0.00000000,
 //  "relayfee": 0.00001000,
 //  "errors": "",
 //  "fork": "Bitcoin Cash"
 //}

```

or

```
 p = Promise.resolve(bcc.getInfo());
 p.then(info=>{
    console.log(info);
 })
```



## Compatible Node Implementations


  You must be running a Node (Pruned mode is fine)

  [Bitcoin ABC](https://www.bitcoinabc.org/)
  [Bitcoin XT ](https://bitcoinxt.software/)
  [Bitcoin Unlimited (Cash)](https://www.bitcoinunlimited.info/)
  [Bitcoin Classic (Cash)](https://bitcoinclassic.com/)



### Tested on Node v7.10, and npm v5.4.1