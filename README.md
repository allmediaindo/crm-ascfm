# Documentati on for the CRM ASCFM APIs

### Public REST API
These are open data for public. It doesn't need an API key to call these methods. You can call simple POST request.

***

## List Users
* The base endpoint is: https://api-crm.techcrm.net/
* All endpoints return either a JSON object or array.
#### Request
| Name | Type | Mandatory | Description |
|-|-|-|-|
| `key` | STRING | yes | API Key |
| `mehod` | STRING | yes | Type method |

#### Response
```json
{
    "result": "success",
    "message": {
        "1468795554": {
            "login": "1468795554",
            "group": "AC-ENTRY",
            "name": "test01",
            "country": "Indonesia",
            "city": "",
            "state": "",
            "zipcode": "",
            "address": "",
            "phone": "",
            "email": "",
            "comment": "",
            "balance": 998.5,
            "prevmonthbalance": 0,
            "prevbalance": 100,
            "equity": 997.57,
            "margin": 6,
            "margin_free": 991.57
        },
        "1468795555": {
            "login": "1468795555",
            "group": "AC-ENTRY",
            "name": "test02",
            "country": "Indonesia",
            "city": "",
            "state": "",
            "zipcode": "1",
            "address": "",
            "phone": "",
            "email": "",
            "comment": "",
            "balance": 1999.7,
            "prevmonthbalance": 0,
            "prevbalance": 0,
            "equity": 1997.23,
            "margin": 16,
            "margin_free": 1981.23
        }
    }
}
```


## List Trades
* The base endpoint is: https://api-crm.techcrm.net/{login}
* All endpoints return either a JSON object or array.
#### Request
| Name | Type | Mandatory | Description | value | Mehod |
|-|-|-|-|-|-|
| `key` | STRING | yes | API Key | | `POST` |
| `method` | STRING | yes | Type method | trades | `POST` |

#### Response
```json
{
    "result": "success",
    "message": [
        {
            "ticket": "3369281",
            "login": "1468795555",
            "order_type": "SELL",
            "symbol": "EURUSD'",
            "volume": 0.01,
            "open_time": "2021-04-08 07:20:16",
            "open_price": 1.19,
            "stop_lose": 0,
            "take_profit": 0,
            "close_time": "1970-01-01 00:00:00",
            "commission": -0.05,
            "swaps": 0,
            "close_price": 1.19,
            "profit": -0.5
        },
        {
            "ticket": "3369282",
            "login": "1468795555",
            "order_type": "SELL",
            "symbol": "EURUSD'",
            "volume": 0.02,
            "open_time": "2021-04-08 07:20:34",
            "open_price": 1.19,
            "stop_lose": 0,
            "take_profit": 0,
            "close_time": "2021-04-08 07:27:22",
            "commission": -0.1,
            "swaps": 0,
            "close_price": 1.19,
            "profit": -0.2
        }
    ]
}
```
