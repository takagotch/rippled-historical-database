### rippled-historical-database
---
https://github.com/ripple/rippled-historical-database

```json
GET /v2/ledgers/xxx

200 OK
{
  "result": "success",
  "ledger": {
    "ledger_hash": "xxx",
    "ledger_index": 8137037,
    "parent_hash": "xxx",
    "total_coins": 99999980165594400,
    "close_time_res": 10,
    "accounts_hash": "xxx",
    "transactions_hash": "xxx",
    "close_time": 1408047740,
    "close_time_human": "2014-08-14T20:20:22:20+00:00"
  }
}
```

```sh
node import/live
node import/hbase/backfill --startIndex 20000000 --stopIndex 1000000
docker-compose build
docker-compose up -d hbase
docker-compose run --rm webapp npm test
git clone https://github.com/ripple/rippled-historical-database.git
cd rippled-histrical-database
npm install
```

```
```
