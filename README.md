
# MultiChain JSON-RPC API Client

## Package Installation

The recommended way to install this library through Composer. Run the Composer command to install the latest stable version:

    composer require rootchips/multichain

## Requirement
```>= PHP 5.4```
```Multichain 2.0```


## Setup

```
<?php

use Chips\Multichain\Client;
use Chips\Multchain\Helper;

$blockchain = new Client(
                    sprintf(
                    'http://%s:%s', '127.0.0.1', '4258'     // Blockchain host and port
                    ),         
                    'multichainrpc',                        // Blockchain username
                    'das858929had88yhfbw37ryw8yh3heyuhebhj', // Blockchain password
                    3
    	      );
 ```
 
 ## Usage
 ```
 $blockchain->setDebug(true)->getInfo()
 ```
 
 ## Result
 ```
 {
    "result": {
        "version": "1.0.5",
        "nodeversion": 10005901,
        "protocolversion": 10011,
        "chainname": "multichain",
        "description": "MultiChain",
        "protocol": "multichain",
        "port": 4259,
        "setupblocks": 60,
        "nodeaddress": "chainname@127.0.0.1:4259",
        "burnaddress": "1XXXXXXWUJXXXXXXVDXXXXXXJbXXXXXXZLkGJr",
        "incomingpaused": false,
        "miningpaused": false,
        "walletversion": 60000,
        "balance": 0,
        "walletdbversion": 2,
        "reindex": false,
        "blocks": 263,
        "timeoffset": 0,
        "connections": 1,
        "proxy": "",
        "difficulty": 6e-8,
        "testnet": false,
        "keypoololdest": 1535212031,
        "keypoolsize": 2,
        "paytxfee": 0,
        "relayfee": 0,
        "errors": ""
    },
    "error": null,
    "id": 1
}
```
