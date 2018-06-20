---
name: IEX
x-slug: iex
description: IEX, the Investors Exchange, is a fair, simple and transparent stock
  exchange dedicated to investor and issuer protection.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
x-kinRank: "9"
x-alexaRank: "225220"
tags: IEX
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/apis.md
specificationVersion: "0.14"
apis:
- name: IEX Trading API Batch Requests
  x-api-slug: iex-trading-api
  description: Returns batch stock quotes.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//stock/market/batch
  tags: Market Data,Quotes,Batch
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/stockmarketbatch-get-openapi.md
- name: IEX Trading API Delayed Quote
  x-api-slug: iex-trading-api
  description: This returns the 15 minute delayed market quote.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//stock/{symbol}/delayed-quote
  tags: Market Data,Quotes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/stocksymboldelayedquote-get-openapi.md
- name: IEX Trading API Earnings
  x-api-slug: iex-trading-api
  description: Pulls data from the four most recent reported quarters.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//stock/{symbol}/earnings
  tags: Market Data,Earnings
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/stocksymbolearnings-get-openapi.md
- name: IEX Trading API Financials
  x-api-slug: iex-trading-api
  description: Pulls income statement, balance sheet, and cash flow data from the
    four most recent reported quarters.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//stock/{symbol}/financials
  tags: Market Data,Financials
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/stocksymbolfinancials-get-openapi.md
- name: IEX Trading API Short Interest List
  x-api-slug: iex-trading-api
  description: Refer to the Short Interest specification for further details
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//stock/{symbol}/short-interest
  tags: Market Data,Short Interest
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/stocksymbolshortinterest-get-openapi.md
- name: IEX Trading API List
  x-api-slug: iex-trading-api
  description: Refer to the quote section.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//stock/{symbol}/list
  tags: Market Data,Quotes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/stocksymbollist-get-openapi.md
- name: IEX Trading API News
  x-api-slug: iex-trading-api
  description: The above example will return JSON with the following keys
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//stock/{symbol}/news/last/{range}
  tags: Market Data,Financial News
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/stocksymbolnewslastrange-get-openapi.md
- name: IEX Trading API Previous
  x-api-slug: iex-trading-api
  description: This returns previous day adjusted price data for a single stock, or
    an object keyed by symbol of price data for the whole market.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//stock/{symbol}/previous
  tags: Market Data,Quotes,Adjustments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/stocksymbolprevious-get-openapi.md
- name: IEX Trading API Quote
  x-api-slug: iex-trading-api
  description: Pulls a stock quote using any ticker symbol.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//stock/{symbol}/quote
  tags: Market Data,Quotes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/stocksymbolquote-get-openapi.md
- name: IEX Trading API Splits
  x-api-slug: iex-trading-api
  description: Returns stock splits for any date range using ticker symbol.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//stock/{symbol}/splits/{range}
  tags: Market Data,Quotes,Splits
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/stocksymbolsplitsrange-get-openapi.md
- name: IEX Trading API Corporate Actions
  x-api-slug: iex-trading-api
  description: Refer to the Daily list specification for futher details.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//ref-data/daily-list/symbol-directory
  tags: Market Data,Daily List
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/refdatadailylistsymboldirectory-get-openapi.md
- name: IEX Trading API Next Day Ex Date
  x-api-slug: iex-trading-api
  description: Refer to the Daily list specification for futher details.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//ref-data/daily-list/next-day-ex-date
  tags: Market Data,Daily List
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/refdatadailylistnextdayexdate-get-openapi.md
- name: IEX Trading API TOPS
  x-api-slug: iex-trading-api
  description: Our eligible symbol reference is updated daily. Use these symbols as
    values in your symbols parameter.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//tops
  tags: Market Data,Tops
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/tops-get-openapi.md
- name: IEX Trading API HIST
  x-api-slug: iex-trading-api
  description: HIST will provide the output of IEX data products for download on a
    T+1 basis. Data will remain available for the trailing twelve months.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//hist
  tags: Market Data,Historical
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/hist-get-openapi.md
- name: IEX Trading API Book
  x-api-slug: iex-trading-api
  description: Subscribe to the book channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//deep/book
  tags: Market Data,Book
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/deepbook-get-openapi.md
- name: IEX Trading API System Event
  x-api-slug: iex-trading-api
  description: Subscribe to the systemevent channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//deep/system-event
  tags: Market Data,System Event
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/deepsystemevent-get-openapi.md
- name: IEX Trading API Operational Halt Status
  x-api-slug: iex-trading-api
  description: Subscribe to the ophaltstatus channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//deep/op-halt-status
  tags: Market Data,Halt Status
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/deepophaltstatus-get-openapi.md
- name: IEX Trading API Security Event
  x-api-slug: iex-trading-api
  description: Subscribe to the securityevent channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//deep/security-event
  tags: Market Data,Security Event
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/deepsecurityevent-get-openapi.md
- name: IEX Trading API Auction
  x-api-slug: iex-trading-api
  description: For an example of an app that&rsquo;s using stats, see our IEX mobile
    app.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//deep/auction
  tags: Market Data,Auctions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/deepauction-get-openapi.md
- name: IEX Trading API Recent
  x-api-slug: iex-trading-api
  description: This call will return a minimum of the last five trading days up to
    all trading days of the current month.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//stats/recent
  tags: Market Data,Statistics
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/statsrecent-get-openapi.md
- name: IEX Trading API Historical Summary
  x-api-slug: iex-trading-api
  description: See our stats page for a reference of the keys.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//stats/historical
  tags: Market Data,Historical
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/statshistorical-get-openapi.md
- name: IEX Trading API Market
  x-api-slug: iex-trading-api
  description: This endpoint returns near real time traded volume on the markets.
    Market data is captured by the IEX system from approximately 7:45 a.m. to 5:15
    p.m. ET.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0//market
  tags: Market Data,Markets
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/market-get-openapi.md
- name: IEX Trading API
  x-api-slug: iex-trading-api
  description: IEX, the Investors Exchange, is a fair, simple and transparent stock
    exchange dedicated to investor and issuer protection.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IEX-Logo.png
  humanURL: https://iextrading.com
  baseURL: https://api.iextrading.com//1.0
  tags: IEX
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/iex/master/_listings/iex/openapi.md
x-common:
- type: x-authentication
  url: https://iextrading.com/developer/docs/#authentication
- type: x-blog
  url: https://medium.com/boxes-and-lines
- type: x-blog-rss
  url: view-source:https://medium.com/feed/boxes-and-lines
- type: x-branding
  url: https://iextrading.com/brand/
- type: x-change-log
  url: https://iextrading.com/developer/docs/#changelog
- type: x-crunchbase
  url: https://crunchbase.com/organization/iex
- type: x-developer
  url: https://iextrading.com/developer/docs/
- type: x-email
  url: sales@iextrading.com
- type: x-email
  url: listings@iextrading.com
- type: x-email
  url: marketops@iextrading.com
- type: x-email
  url: sre@iextrading.com
- type: x-email
  url: marcomms@iextrading.com
- type: x-email
  url: info@iextrading.com
- type: x-email
  url: api@iextrading.com
- type: x-email
  url: legal@iextrading.com
- type: x-email
  url: ventures@iextrading.com
- type: x-faq
  url: https://iextrading.com/faq/
- type: x-github
  url: https://github.com/iexg
- type: x-linkedin
  url: https://www.linkedin.com/company/iex-group-inc-
- type: x-press
  url: https://iextrading.com/about/press/
- type: x-road-map
  url: https://iextrading.com/developer/docs/#roadmap
- type: x-terms-of-service
  url: https://iextrading.com/developer/docs/#terms
- type: x-twitter
  url: https://twitter.com/IEX
- type: x-website
  url: https://iextrading.com
- type: x-websockets
  url: https://iextrading.com/developer/docs/#websockets
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---