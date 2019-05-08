# ![LOGO](logo.png) Yunbi **flow**ground Connector

## Description

A generated **flow**ground connector for the Yunbi API (version v2).

Generated from: https://api.apis.guru/v2/specs/yunbi.com/v2/swagger.json<br/>
Generated at: 2019-05-07T17:45:05+03:00

## API Description

Professional Cloud Trading Platform for Digital Assets

## Authorization

This API does not require authorization.

## Actions

### Check Deposit Address

*Tags:* `addresses`

#### Input Parameters
* `address` - _required_

### Get details of specific deposit.

*Tags:* `deposit`

#### Input Parameters
* `access_key` - _required_ - Access key.
* `tonce` - _required_ - Tonce is an integer represents the milliseconds elapsed since Unix epoch.
* `signature` - _required_ - The signature of your request payload, generated using your secret key.
* `txid` - _required_

### Where to deposit. The address field could be empty when a new address is generating (e.g. for bitcoin), you should try again later in that case.

*Tags:* `deposit_address`

#### Input Parameters
* `access_key` - _required_ - Access key.
* `tonce` - _required_ - Tonce is an integer represents the milliseconds elapsed since Unix epoch.
* `signature` - _required_ - The signature of your request payload, generated using your secret key.
* `currency` - _required_ - The account to which you want to deposit. Available values: cny, btc, eth, pls, note, bts, bitcny, bitusd, bitbtc, yun, nxt, ltc, doge, sc, dgd, dcs, dao, etc, amp, 1st, rep, ans, zec, zmc, gnt, gxs, qtum, eos, snt, bcc, omg, lun, pay, ven

### Get your deposits history.

*Tags:* `deposits`

#### Input Parameters
* `access_key` - _required_ - Access key.
* `tonce` - _required_ - Tonce is an integer represents the milliseconds elapsed since Unix epoch.
* `signature` - _required_ - The signature of your request payload, generated using your secret key.
* `currency` - _optional_ - Currency value contains  cny, btc, eth, pls, note, bts, bitcny, bitusd, bitbtc, yun, nxt, ltc, doge, sc, dgd, dcs, dao, etc, amp, 1st, rep, ans, zec, zmc, gnt, gxs, qtum, eos, snt, bcc, omg, lun, pay, ven
* `limit` - _optional_ - Set result limit.
* `state` - _optional_ - State value contains  submitting, cancelled, submitted, rejected, accepted, checked, warning

### Get depth or specified market. Both asks and bids are sorted from highest price to lowest.

*Tags:* `depth`

#### Input Parameters
* `market` - _required_ - Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btccny'. All available markets can be found at /api/v2/markets.
* `limit` - _optional_ - Limit the number of returned price levels. Default to 300.

### Get OHLC(k line) of specific market.

*Tags:* `k`

#### Input Parameters
* `market` - _required_ - Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btccny'. All available markets can be found at /api/v2/markets.
* `limit` - _optional_ - Limit the number of returned data points, default to 30.
* `period` - _optional_ - Time period of K line, default to 1. You can choose between 1, 5, 15, 30, 60, 120, 240, 360, 720, 1440, 4320, 10080
* `timestamp` - _optional_ - An integer represents the seconds elapsed since Unix epoch. If set, only k-line data after that time will be returned.

### Get K data with pending trades, which are the trades not included in K data yet, because there's delay between trade generated and processed by K data generator.

*Tags:* `k_with_pending_trades`

#### Input Parameters
* `market` - _required_ - Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btccny'. All available markets can be found at /api/v2/markets.
* `trade_id` - _required_ - The trade id of the first trade you received.
* `limit` - _optional_ - Limit the number of returned data points, default to 30.
* `period` - _optional_ - Time period of K line, default to 1. You can choose between 1, 5, 15, 30, 60, 120, 240, 360, 720, 1440, 4320, 10080
* `timestamp` - _optional_ - An integer represents the seconds elapsed since Unix epoch. If set, only k-line data after that time will be returned.

### Get all available markets.

*Tags:* `markets`

### Get your profile and accounts info.

*Tags:* `members`

#### Input Parameters
* `access_key` - _required_ - Access key.
* `tonce` - _required_ - Tonce is an integer represents the milliseconds elapsed since Unix epoch.
* `signature` - _required_ - The signature of your request payload, generated using your secret key.

### Get information of specified order.

*Tags:* `order`

#### Input Parameters
* `access_key` - _required_ - Access key.
* `tonce` - _required_ - Tonce is an integer represents the milliseconds elapsed since Unix epoch.
* `signature` - _required_ - The signature of your request payload, generated using your secret key.
* `id` - _required_ - Unique order id.

### Cancel an order.

*Tags:* `order`

### Get the order book of specified market.

*Tags:* `order_book`

#### Input Parameters
* `market` - _required_ - Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btccny'. All available markets can be found at /api/v2/markets.
* `asks_limit` - _optional_ - Limit the number of returned sell orders. Default to 20.
* `bids_limit` - _optional_ - Limit the number of returned buy orders. Default to 20.

### Get your orders, results is paginated.

*Tags:* `orders`

#### Input Parameters
* `access_key` - _required_ - Access key.
* `tonce` - _required_ - Tonce is an integer represents the milliseconds elapsed since Unix epoch.
* `signature` - _required_ - The signature of your request payload, generated using your secret key.
* `market` - _required_ - Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btccny'. All available markets can be found at /api/v2/markets.
* `state` - _optional_ - Filter order by state. One of 'wait', 'done', or 'cancel'. An order in 'wait' is an active order, waiting fullfillment; a 'done' order is an order fullfilled; 'cancel' means the order has been cancelled. Default to 'wait'.
* `limit` - _optional_ - Limit the number of returned orders, default to 100.
* `page` - _optional_ - Specify the page of paginated results.
* `order_by` - _optional_ - If set, returned orders will be sorted in specific order. One of 'asc' or 'desc', default to 'asc'.

### Create a Sell/Buy order.

*Tags:* `orders`

### Cancel all my orders.

*Tags:* `orders`

### Create multiple sell/buy orders.

*Tags:* `orders`

### GET__version_partners_orders__id_trades___format_

*Tags:* `partners`

#### Input Parameters
* `id` - _required_
* `access_key_hash` - _required_

### Get ticker of all markets.

*Tags:* `tickers`

### Get ticker of specific market.

*Tags:* `tickers`

#### Input Parameters
* `market` - _required_ - Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btccny'. All available markets can be found at /api/v2/markets.

### Get server current time, in seconds since Unix epoch.

*Tags:* `timestamp`

### Get recent trades on market, each trade is included only once. Trades are sorted in reverse creation order.

*Tags:* `trades`

#### Input Parameters
* `market` - _required_ - Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btccny'. All available markets can be found at /api/v2/markets.
* `limit` - _optional_ - Limit the number of returned trades. Default to 50.
* `timestamp` - _optional_ - An integer represents the seconds elapsed since Unix epoch. If set, only trades executed before the time will be returned.
* `from` - _optional_ - Trade id. If set, only trades created after the trade will be returned.
* `to` - _optional_ - Trade id. If set, only trades created before the trade will be returned.
* `order_by` - _optional_ - If set, returned trades will be sorted in specific order. One of 'asc' or 'desc', default to 'desc'.

### Get your executed trades. Trades are sorted in reverse creation order.

*Tags:* `trades`

#### Input Parameters
* `access_key` - _required_ - Access key.
* `tonce` - _required_ - Tonce is an integer represents the milliseconds elapsed since Unix epoch.
* `signature` - _required_ - The signature of your request payload, generated using your secret key.
* `market` - _required_ - Unique market id. It's always in the form of xxxyyy, where xxx is the base currency code, yyy is the quote currency code, e.g. 'btccny'. All available markets can be found at /api/v2/markets.
* `limit` - _optional_ - Limit the number of returned trades. Default to 50.
* `timestamp` - _optional_ - An integer represents the seconds elapsed since Unix epoch. If set, only trades executed before the time will be returned.
* `from` - _optional_ - Trade id. If set, only trades created after the trade will be returned.
* `to` - _optional_ - Trade id. If set, only trades created before the trade will be returned.
* `order_by` - _optional_ - If set, returned trades will be sorted in specific order. One of 'asc' or 'desc', default to 'desc'.

## License

**flow**ground :- Telekom iPaaS / yunbi-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
