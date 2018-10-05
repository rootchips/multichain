
# MultiChain JSON-RPC API Client

## Installation

The recommended way to install this library through Composer. Run the Composer command to install the latest stable version:

    composer require rootchips/multichain

## Requirement
```>= PHP 5.4```
```Multichain 2.0```


## Setup

```php
<?php

use Chips\Multichain\Client;

$blockchain = new Client(
                    sprintf(
                    'https://%s:%s', '127.0.0.1', '4258'     // Blockchain host and port
                    ),         
                    'multichainrpc',                        // Blockchain username
                    'das858929had88yhfbw37ryw8yh3heyuhebhj', // Blockchain password
                    3
    	      );
 ```
 
 ## Usage: Publish data to stream
 ```php
 $blockchain->publish('stream1', 'key', 'data');
 ```
 
 ## Result
 ```json
{
    "result": "a92f7e9520df83999fca41f44f0e0434e9b802a54d2737b5ae548decbb49e321", // transaction id
    "error": null,
    "id": 1
}
```


## Usage: Retrieve the data by passing transaction id
```php
$blockchain->gettxoutdata('a92f7e9520df83999fca41f44f0e0434e9b802a54d2737b5ae548decbb49e321', 0, 1024);
```


## Result
```json
{
    "result": "1234",
    "error": null,
    "id": 1
}
```

