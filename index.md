# **Welcome to Liberary-Cpp Document**

Liberary-Cpp는 [(주)리베라](https://www.libera.or.kr)의 가상자산 알고리즘 트레이딩 전용 C++ Library입니다.
Source Code는 공개되지 않으며, Software License 문의는 아래로 연락바랍니다.  
Liberary-Cpp is a C++ Library for crypto currency algorithm traiding of [Libera Inc.](https://www.libera.or.kr)
Source code will not be disclosed, so please contact below for inquiries about the Software License.

CEO 곽동훈(Donghoon Gwag) | 010-9549-0188 | <ceo@libera.or.kr>

---

## **Dependencies**

|Package Name           |Version                  |
|-----------------------|-------------------------|
|g++                    |4:7.4.0-1ubuntu2.3       |
|boost                  |1.78.0                   |
|libtbb-dev             |2017~U7-8                |
|rapidjson-dev          |1.1.0+dfsg2-3            |
|libssl-dev             |1.1.1-1ubuntu2.1~18.04.15|
|libcurl4-openssl-dev   |7.58.0-2ubuntu3.16       |
|jwt-cpp (github)       |v0.6.0 (hash:4a537e9)    |
|zlib1g-dev             |1:1.2.11.dfsg-0ubuntu2.1 |

---

## **Abstraction**
O : Implemented  
△ : Not implemented but will be supported  
X : Not implemented and will not be supported  
  
**Spot**

|                                                                  | Upbit | Bithumb | Huobi | Binance | Okx | Ftx |
|------------------------------------------------------------------|-------|---------|-------|---------|-----|-----|
| setErrorLogger(*logger)                                          | O     | O       | O     | O       | O   | O   |
| getMarketCurrencies(market)                                      | O     | O       | O     | O       | O   | O   |
| updateTradingFee()                                               | O     | O       | O     | O       | O   | O   |
| getTradingFee(currency, market)                                  | O     | O       | O     | O       | O   | O   |
| orderLimitBuy(currency, market, price, amount)                   | O     | O       | O     | O       | O   | O   |
| orderLimitSell(currency, market, price, amount)                  | O     | O       | O     | O       | O   | O   |
| orderLimitBuyAmplify(currency, market, price, amount, amplifier) | O     | O       | O     | O       | O   | O   |
| orderLimitSellAmplify(currency, market, price, amount, amplifier)| O     | O       | O     | O       | O   | O   |
| orderInfo(currency, market, id)                                  | O     | O       | O     | O       | O   | O   |
| orderCancel(currency, market, id)                                | O     | O       | O     | O       | O   | O   |
| withdraw(currency, amount, address, tag, chain)                  | O     | △       | O     | O       | O   | O   |
| getWithdrawAmount(currency, since, id)                           | O     | O       | O     | O       | O   | O   |
| getWithdrawList(since)                                           | O     | △       | △     | △       | △   | △   |
| updateAccountBalance()                                           | O     | O       | O     | O       | O   | O   |
| updateAccountBalance(currencies)                                 | O     | O       | O     | O       | O   | O   |
| getAccountBalance(currency)                                      | O     | O       | O     | O       | O   | O   |
| getAllAccountBalance()                                           | O     | O       | O     | O       | O   | O   |
| updateWithdrawStatus()                                           | O     | O       | O     | O       | O   | O   |
| getWithdrawStatus(currency, chain)                               | O     | O       | O     | O       | O   | O   |
| isDepositCompleted(currency, amount, int64_t since)              | O     | O       | O     | O       | O   | O   |
| getOpenOrders(marketList)                                        | O     | X       | O     | O       | O   | O   |
| getOpenOrders(currency, market)                                  | △     | O       | △     | △       | △   | △   |
| getCandleData(currency, market, interval, startTime, endTime)    | O     | O       | △     | O       | △   | O   |
| updateAllOrderbook(market)                                       | △     | O       | △     | △       | △   | △   |
| updateOrderbook(currency, market)                                | △     | O       | △     | △       | △   | △   |
| websocketDepth(pairs)                                            | O     | O       | O     | O       | O   | O   |
| orderbookSubscribe(pairs)                                        | O     | O       | △     | O       | O   | O   |
| orderbookUnsubscribe(pairs)                                      | O     | O       | △     | O       | O   | O   |
| websocketUserStream()                                            | X     | X       | O     | O       | △   | X   |
| getOrderbook(currency, market)                                   | O     | O       | O     | O       | O   | O   |

**Futures**

|                                                                                        | Binance | Ftx |
|----------------------------------------------------------------------------------------|---------|-----|
| getMarketCurrencies(market)                                                            | O       | O   |
| orderLimitBuy(currency, market, expiration, price, amount)                             | O       | O   |
| orderLimitSell(currency, market, expiration, price, amount)                            | O       | O   |
| orderLimitBuyAmplify(currency, market, expiration, price, amount, amplifier)           | O       | O   |
| orderLimitSellAmplify(currency, market, expiration, price, amount, amplifier)          | O       | O   |
| changeLeverage(currency, market, expiration, leverage)                                 | O       | O   |
| changeMarginType(currency, market, expiration, margin)                                 | O       | X   |
| updateAccountInfo()                                                                    | O       | O   |
| getTotalMarginBalance()                                                                | O       | O   |
| getLeverage(currency, market, expiration)                                              | O       | O   |
| getMarginType(currency, market, expiration)                                            | O       | O   |
| getPositionAmt(currency, market, expiration)                                           | O       | O   |
| getAllPositionAmt()                                                                    | O       | O   |
| getFundingFees(since)                                                                  | O       | O   |
| getCandleData(currency, market, expiration, interval, startTime, endTime)              | O       | O   |
| websocketDepth(pairs)                                                                  | O       | O   |
| orderbookSubscribe(pairs)                                                              | O       | O   |
| orderbookUnsubscribe(pairs)                                                            | O       | O   |

---

Copyright © Libera Inc. All rights reserved
