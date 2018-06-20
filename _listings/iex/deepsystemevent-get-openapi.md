---
swagger: "2.0"
x-collection-name: IEX
x-complete: 0
info:
  title: IEX Trading API System Event
  description: Subscribe to the systemevent channel.
  termsOfService: https://iextrading.com/api-terms/
  version: 1.0.0
host: api.iextrading.com
basePath: /1.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
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
  /stock/{symbol}/previous:
    get:
      summary: Previous
      description: This returns previous day adjusted price data for a single stock,
        or an object keyed by symbol of price data for the whole market.
      operationId: previous
      x-api-path-slug: stocksymbolprevious-get
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
      - Adjustments
  /stock/{symbol}/quote:
    get:
      summary: Quote
      description: Pulls a stock quote using any ticker symbol.
      operationId: quote
      x-api-path-slug: stocksymbolquote-get
      parameters:
      - in: query
        name: displayPercent
        description: 'Optional If set to true, all percentage values will be multiplied
          by a factor of 100 (Ex: /stock/aapl/quote?displayPercent=true)'
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
  /stock/{symbol}/splits/{range}:
    get:
      summary: Splits
      description: Returns stock splits for any date range using ticker symbol.
      operationId: splits
      x-api-path-slug: stocksymbolsplitsrange-get
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
      - Quotes
      - Splits
  /ref-data/daily-list/symbol-directory:
    get:
      summary: Corporate Actions
      description: Refer to the Daily list specification for futher details.
      operationId: iex-corporate-actions
      x-api-path-slug: refdatadailylistsymboldirectory-get
      parameters:
      - in: query
        name: format
        description: Parameter is optional Value can be csv or psv When parameter
          is not present, format defaults to JSON
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
      - Daily List
  /ref-data/daily-list/next-day-ex-date:
    get:
      summary: Next Day Ex Date
      description: Refer to the Daily list specification for futher details.
      operationId: iex-next-day-ex-date
      x-api-path-slug: refdatadailylistnextdayexdate-get
      parameters:
      - in: query
        name: format
        description: Parameter is optional Value can be csv or psv When parameter
          is not present, format defaults to JSON
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
      - Daily List
  /tops:
    get:
      summary: TOPS
      description: Our eligible symbol reference is updated daily. Use these symbols
        as values in your symbols parameter.
      operationId: tops
      x-api-path-slug: tops-get
      parameters:
      - in: query
        name: format
        description: Parameter is optional Value can only be csv When parameter is
          not present, format defaults to JSON
      - in: query
        name: symbols
        description: Parameter is optional Value needs to be a comma-separated list
          of symbols (i
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Tops
  /hist:
    get:
      summary: HIST
      description: HIST will provide the output of IEX data products for download
        on a T+1 basis. Data will remain available for the trailing twelve months.
      operationId: hist
      x-api-path-slug: hist-get
      parameters:
      - in: query
        name: date
        description: Parameter is optional Value needs to be in four-digit year, two-digit
          month, two-digit day format (YYYYMMDD) (i
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Historical
  /deep/book:
    get:
      summary: Book
      description: Subscribe to the book channel.
      operationId: book
      x-api-path-slug: deepbook-get
      parameters:
      - in: query
        name: symbols
        description: Parameter is required Value needs to be a comma-separated list
          of symbols (i
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Book
  /deep/system-event:
    get:
      summary: System Event
      description: Subscribe to the systemevent channel.
      operationId: system-event
      x-api-path-slug: deepsystemevent-get
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - System Event
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---