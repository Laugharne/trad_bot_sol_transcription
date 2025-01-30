🔴 Let's code a trading bot for Solana! - Video Highlights

# [00:00](https://youtu.be/9vG59d2HBMM?t=0)  How to Create a Trading Bot on SOL

## Introduction to the Host and Topic
- [00:00](https://youtu.be/9vG59d2HBMM?t=0)  Julian introduces himself as the host of the live stream, focusing on creating a trading bot on Solana (SOL).
- [00:39](https://youtu.be/9vG59d2HBMM?t=39)  He emphasizes the advantages of using trading bots, such as eliminating human psychology and discipline issues in trading.

## Free Training Announcement
- [01:13](https://youtu.be/9vG59d2HBMM?t=73)  Julian promotes his free training available at ethblocks.com, aimed at beginners wanting to become professional blockchain developers.

## Overview of Trading Strategy
- [01:47](https://youtu.be/9vG59d2HBMM?t=107)  The chosen strategy for the trading bot is based on moving averages, which track asset prices over time.
- [02:25](https://youtu.be/9vG59d2HBMM?t=145)  Different types of moving averages are discussed (e.g., 200-day, 90-day), highlighting their effectiveness in indicating trend changes.

## Understanding Moving Averages
- [03:00](https://youtu.be/9vG59d2HBMM?t=180)  Julian explains that crossing above or below a moving average can signal bullish or bearish trends respectively.

## Technical Setup for Coding
- [03:37](https://youtu.be/9vG59d2HBMM?t=217)  Node.js will be used for coding due to its versatility across different operating systems.
- [04:11](https://youtu.be/9vG59d2HBMM?t=251)  The CoinGecko API will provide price data necessary for the bot's functionality; it offers a free tier with limited requests.

## Exchange Integration
- [05:07](https://youtu.be/9vG59d2HBMM?t=307)  To execute trades automatically, access to an exchange's API is required.
- [05:40](https://youtu.be/9vG59d2HBMM?t=340)  While decentralized exchanges can be used, centralized exchanges like Coinbase or Binance are recommended for ease of use.

## Tools and Libraries Required
- [06:04](https://youtu.be/9vG59d2HBMM?t=364)  CCXT is introduced as a JavaScript library that simplifies interaction with various exchange APIs through a unified interface.

## Starting the Coding Process
# [08:42](https://youtu.be/9vG59d2HBMM?t=522)  Installation and Setup of Environment Variables

## Installing Required Packages
- [08:42](https://youtu.be/9vG59d2HBMM?t=522)  The speaker begins by discussing the installation of necessary packages, specifically `M` for reading environment variables and `ccxt`, a library for cryptocurrency trading.
- [09:18](https://youtu.be/9vG59d2HBMM?t=558)  A script named `script.js` is created to load environment variables using the `M` package, which will help manage sensitive information like API keys.

## Creating an API Key
- [10:00](https://youtu.be/9vG59d2HBMM?t=600)  Instructions are provided on how to create a CoinGecko API key by signing up for a free account and selecting the demo tier, which is not clearly labeled as "free."
- [10:33](https://youtu.be/9vG59d2HBMM?t=633)  The speaker emphasizes that users do not need to purchase anything to access the free tier; they should simply locate the demo option.
# [11:07](https://youtu.be/9vG59d2HBMM?t=667)  Understanding CoinGecko's API Endpoints

## Identifying Necessary Endpoints
- [11:07](https://youtu.be/9vG59d2HBMM?t=667)  The speaker navigates through CoinGecko's documentation to find relevant API endpoints, focusing on historical data retrieval.
- [11:56](https://youtu.be/9vG59d2HBMM?t=716)  The specific endpoint discussed allows users to obtain historical chart data for cryptocurrencies, including price and market cap over specified time frames.

## Parameters for Historical Data Retrieval
- [12:33](https://youtu.be/9vG59d2HBMM?t=753)  Key parameters include specifying the coin ID (e.g., Solana), currency (usually USD), number of days of historical data required, and interval settings.
- [13:07](https://youtu.be/9vG59d2HBMM?t=787)  The response from this endpoint includes arrays containing timestamps along with corresponding prices and market caps.
# [13:29](https://youtu.be/9vG59d2HBMM?t=809)  Constructing the API Call in JavaScript

## Building the Request URL
- [13:29](https://youtu.be/9vG59d2HBMM?t=809)  The speaker explains how to construct the request URL by removing "pro" from it since they are using a free version of the API.
- [14:39](https://youtu.be/9vG59d2HBMM?t=879)  Query strings are added to specify parameters such as currency type (`usd`), interval (`daily`), number of days (7), and inclusion of an API key read from environment variables.

## Implementing Async Functionality
- [15:36](https://youtu.be/9vG59d2HBMM?t=936)  An asynchronous function is defined to handle fetching data from the constructed URL. This function will utilize JavaScript's `fetch()` method.
- [16:11](https://youtu.be/9vG59d2HBMM?t=971)  Headers are set up in this function to indicate that both requests and responses will be in JSON format.
# [16:51](https://youtu.be/9vG59d2HBMM?t=1011)  Executing and Testing the Script

## Making HTTP Requests
- [16:51](https://youtu.be/9vG59d2HBMM?t=1011)  After setting up headers, a console log statement is included for debugging purposes, allowing verification that everything functions correctly before running it.
# [19:01](https://youtu.be/9vG59d2HBMM?t=1141)  Understanding Moving Averages in Trading Bots

## Analyzing Market Data
- [19:01](https://youtu.be/9vG59d2HBMM?t=1141)  The speaker discusses the total volume, market cap, and prices of a cryptocurrency, indicating that the current price is 170.
- [19:36](https://youtu.be/9vG59d2HBMM?t=1176)  The timestamp is converted to a date (Thursday, May 23rd), confirming that the data was retrieved approximately 20 minutes ago.

## Computing Moving Averages
- [20:23](https://youtu.be/9vG59d2HBMM?t=1223)  To compute the moving average, the speaker plans to use an object called `doPrices` with a `reduce` function to transform an array into a single number.
- [20:59](https://youtu.be/9vG59d2HBMM?t=1259)  The first step involves summing all prices while selecting only the second column of data (the price), initializing the reducer with zero for accurate calculations.

## Iterative Summation Process
- [21:35](https://youtu.be/9vG59d2HBMM?t=1295)  The iterative process builds up a sum by adding each new price to the previously computed sum. This continues until all elements are processed.
- [22:09](https://youtu.be/9vG59d2HBMM?t=1329)  The speaker realizes they need to adjust their approach since they initially miscounted elements; they decide to remove the last element from their array.

## Adjusting Array Length
- [23:01](https://youtu.be/9vG59d2HBMM?t=1381)  After researching JavaScript's `pop` method, it’s confirmed that it removes and returns the last element of an array while changing its length in place.
- [23:36](https://youtu.be/9vG59d2HBMM?t=1416)  By using this method, they can ensure only seven elements remain in their prices array for accurate moving average calculation.

## Finalizing Average Calculation
- [24:13](https://youtu.be/9vG59d2HBMM?t=1453)  The calculated moving average will be stored in a variable named `average`, which will then be logged for verification.
- [24:26](https://youtu.be/9vG59d2HBMM?t=1466)  Upon running the script, an output of approximately 173 confirms that calculations are functioning correctly.

## Verifying Data Accuracy
- [25:10](https://youtu.be/9vG59d2HBMM?t=1510)  The speaker emphasizes testing as crucial when running trading bots; they meticulously check previous data against their calculations.
- [26:10](https://youtu.be/9vG59d2HBMM?t=1570)  After verifying computations yield an average of 173.21, confidence in code accuracy increases before proceeding further.

## Fetching Current Prices
- [26:55](https://youtu.be/9vG59d2HBMM?t=1615)  Plans are made to fetch current prices for comparison against moving averages; unnecessary console logs will be removed from previous steps.
- [27:31](https://youtu.be/9vG59d2HBMM?t=1651)  They identify necessary API endpoints from CoinGecko documentation for retrieving real-time coin prices based on coin ID.

## Setting Up API Requests
- [28:07](https://youtu.be/9vG59d2HBMM?t=1687)  Adjustments are made to set up API URLs correctly; parameters such as currency and IDs must be specified accurately for successful requests.
# [30:11](https://youtu.be/9vG59d2HBMM?t=1811)  Using API to Fetch Current Price

## Setting Up the API Call
- [30:11](https://youtu.be/9vG59d2HBMM?t=1811)  The discussion begins with the need to utilize an endpoint API URL for fetching price data.
- [30:24](https://youtu.be/9vG59d2HBMM?t=1824)  The speaker mentions copying existing code to define parameters for the API call, aiming to transform the response into JSON format and extract the current price in USD.

## Debugging Issues
- [31:25](https://youtu.be/9vG59d2HBMM?t=1885)  After running the script, a missing 'await' keyword is identified as a source of error.
- [31:45](https://youtu.be/9vG59d2HBMM?t=1905)  Further debugging reveals a missing parameter ('vs_currencies') which is corrected by changing it from singular to plural.

## Handling API Throttling
- [32:38](https://youtu.be/9vG59d2HBMM?t=1958)  The speaker encounters throttling from the API due to usage patterns that do not align with expected behavior, leading to temporary blocking.
- [33:03](https://youtu.be/9vG59d2HBMM?t=1983)  After resolving issues, they successfully retrieve a current price close to expectations, confirming functionality.
# [33:39](https://youtu.be/9vG59d2HBMM?t=2019)  Comparing Prices and Moving Averages

## Discussion on Data Sources
- [33:39](https://youtu.be/9vG59d2HBMM?t=2019)  A question arises about whether it's easier to obtain Open High Low Close (OHLC) data directly from CCXT instead of CoinGecko.
- [34:03](https://youtu.be/9vG59d2HBMM?t=2043)  The speaker prefers CoinGecko for its average pricing across multiple exchanges, arguing it provides a more accurate market representation compared to individual exchange data.

## Trading Strategy Development
- [34:26](https://youtu.be/9vG59d2HBMM?t=2066)  The focus shifts towards comparing current prices against moving averages; determining if buying when above or below makes sense.
- [35:01](https://youtu.be/9vG59d2HBMM?t=2101)  It’s established that generally, buying when above moving averages indicates upward trends while below suggests downward trends.
# [35:52](https://youtu.be/9vG59d2HBMM?t=2152)  Implementing Trading Parameters

## Defining Trade Conditions
- [35:52](https://youtu.be/9vG59d2HBMM?t=2152)  If the current price exceeds the moving average, trading will be initiated.
- [36:28](https://youtu.be/9vG59d2HBMM?t=2188)  A limit order will be placed with defined maximum buying prices set at 2% above the current price based on market conditions.

## Risk Management Strategies
- [36:51](https://youtu.be/9vG59d2HBMM?t=2211)  Discussion includes understanding bid/ask spreads and how they affect trading decisions; emphasizing that trades are never executed at mid rates but rather at either bid or ask prices.
### Stop Loss and Take Profit Mechanisms
- [38:01](https://youtu.be/9vG59d2HBMM?t=2281)  Two key parameters are introduced: stop loss (to protect against losses if trades move unfavorably), and take profit (to secure gains when trades go well).
# [39:54](https://youtu.be/9vG59d2HBMM?t=2394)  Understanding Asymmetrical Gains in Trading

## Importance of Take Profit and Stop Loss
- [39:54](https://youtu.be/9vG59d2HBMM?t=2394)  It is crucial to set a take profit that exceeds the stop loss to achieve asymmetrical gains, meaning winning more than losing.
- [40:17](https://youtu.be/9vG59d2HBMM?t=2417)  If wins and losses are equal but profits and losses are the same, the net profit will be zero; thus, it's essential to ensure that wins outweigh losses.

## Setting Up Trading Parameters
- [40:41](https://youtu.be/9vG59d2HBMM?t=2441)  The discussion transitions into setting parameters for placing buy orders using the CCXT library.
- [41:22](https://youtu.be/9vG59d2HBMM?t=2482)  An exchange object must be instantiated by specifying the exchange name (e.g., Binance), along with API keys for authentication.

## API Key Configuration
- [42:09](https://youtu.be/9vG59d2HBMM?t=2529)  Users need to read their API key from environment variables and define it in their configuration files.
- [43:03](https://youtu.be/9vG59d2HBMM?t=2583)  It's recommended to create an API key with minimal privileges, specifically allowing only order creation without withdrawal capabilities.

## Creating Buy Orders
- [43:48](https://youtu.be/9vG59d2HBMM?t=2628)  To place a buy order, several variables must be defined: symbol (e.g., Sol USD), order type (limit order), and amount based on budget.
- [44:20](https://youtu.be/9vG59d2HBMM?t=2660)  The current price can dynamically adjust how much of an asset is purchased; for example, buying 5 Solana at $170 each totals around $1,000 per trade.

## Executing Orders and Handling Feedback
- [45:28](https://youtu.be/9vG59d2HBMM?t=2728)  The `create_order` function from CCXT is used to execute the buy order with specified parameters including symbol, type, side (buy/sell), amount, limit price, and additional parameters like stop loss and take profit.
- [48:21](https://youtu.be/9vG59d2HBMM?t=2901)  After creating an order successfully, feedback should be logged detailing the transaction's specifics such as amount, symbol, limit price, take profit level, and stop loss.

## Automating Trade Execution
# [49:55](https://youtu.be/9vG59d2HBMM?t=2995)  How to Implement a Daily Trading Strategy

## Overview of the Daily Trading Strategy
- [49:55](https://youtu.be/9vG59d2HBMM?t=2995)  The strategy involves checking the moving average of the last seven days daily, comparing it to the current price, and then taking a position based on this analysis.
- [49:55](https://youtu.be/9vG59d2HBMM?t=2995)  Users can monitor all created positions within their exchange platform after executing this trading bot.

## Testing Methods for the Trading Bot
- [50:28](https://youtu.be/9vG59d2HBMM?t=3028)  It is recommended to utilize the testing mode offered by crypto exchanges like Binance, allowing users to trade with paper money as a risk-free way to evaluate strategies.
- [50:28](https://youtu.be/9vG59d2HBMM?t=3028)  Backtesting is another method where traders apply their strategies using historical data. This helps in understanding potential performance without real financial risk.

## Importance of Backtesting
- [51:02](https://youtu.be/9vG59d2HBMM?t=3062)  While past performance does not guarantee future results, backtesting provides insights into how different parameters might affect profitability.
- [51:02](https://youtu.be/9vG59d2HBMM?t=3062)  Traders can experiment with various settings during backtesting until they identify configurations that yield profits.

## Conclusion and Resources

---

📺 [Watch the full video](https://youtu.be/9vG59d2HBMM)

