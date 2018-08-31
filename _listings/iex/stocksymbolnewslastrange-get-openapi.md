---
swagger: "2.0"
x-collection-name: IEX
x-complete: 0
info:
  title: IEX Trading API News
  description: The above example will return JSON with the following keys
  termsOfService: https://iextrading.com/api-terms/
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
host: api.iextrading.com
basePath: /1.0
paths:
  /stock/market/batch:
    get:
      summary: Batch Requests
      description: Returns batch stock quotes.
      operationId: batch-requests
      x-api-path-slug: stockmarketbatch-get
      parameters:
      - ~
      - in: query
        name: range
        description: Optional  Used to specify a chart range if chart is used in types
          parameter
      - in: query
        name: symbols
        description: Optional  Comma delimited list of symbols limited to 100
      - in: query
        name: types
        description: Required  Comma delimited list of endpoints to call
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Quotes
      - Batch
  /stock/{symbol}/delayed-quote:
    get:
      summary: Delayed Quote
      description: This returns the 15 minute delayed market quote.
      operationId: delayed-quote
      x-api-path-slug: stocksymboldelayedquote-get
      parameters:
      - in: path
        name: symbol
        description: Stock ticker symbol
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Quotes
  /stock/{symbol}/earnings:
    get:
      summary: Earnings
      description: Pulls data from the four most recent reported quarters.
      operationId: earnings
      x-api-path-slug: stocksymbolearnings-get
      parameters:
      - in: path
        name: symbol
        description: Stock ticker symbol
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Earnings
  /stock/{symbol}/financials:
    get:
      summary: Financials
      description: Pulls income statement, balance sheet, and cash flow data from
        the four most recent reported quarters.
      operationId: financials
      x-api-path-slug: stocksymbolfinancials-get
      parameters:
      - in: path
        name: symbol
        description: Stock ticker symbol
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Financials
  /stock/{symbol}/short-interest:
    get:
      summary: Short Interest List
      description: Refer to the Short Interest specification for further details
      operationId: iex-short-interest-list
      x-api-path-slug: stocksymbolshortinterest-get
      parameters:
      - in: query
        name: format
        description: Parameter is optional Value can be csv or psv When parameter
          is not present, format defaults to JSON
      - in: path
        name: symbol
        description: Stock ticker symbol
        type: string
        format: string
      - in: query
        name: token
        description: Parameter is optional Value is the API token from your IEX user
          account If you have been permissioned for CUSIP information you&rsquo;ll
          receive a CUSIP field, othewise data defaults to exclude CUSIP
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Short Interest
  /stock/{symbol}/list:
    get:
      summary: List
      description: Refer to the quote section.
      operationId: list
      x-api-path-slug: stocksymbollist-get
      parameters:
      - in: query
        name: displayPercent
        description: 'Optional  If set to true, all percentage values will be multiplied
          by a factor of 100 (Ex: /stock/aapl/quote?displayPercent=true)'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Quotes
  /stock/{symbol}/news/last/{range}:
    get:
      summary: News
      description: The above example will return JSON with the following keys
      operationId: news
      x-api-path-slug: stocksymbolnewslastrange-get
      parameters:
      - in: path
        name: range
        description: The date range
        type: string
        format: string
      - in: path
        name: symbol
        description: Stock ticker symbol
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Financial News
x-streamrank:
  polling_total_time_average: "0.27"
  polling_size_download_average: "13553"
  streaming_total_time_average: "0.18"
  streaming_size_download_average: "6865.88"
  change_yes: "180"
  change_no: "2871"
  time_percentage: "34"
  size_percentage: "49"
  change_percentage: "6"
  last_run: "2018-02-20"
  days_run: "6"
  minute_run: "0"
---