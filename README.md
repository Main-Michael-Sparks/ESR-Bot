
# Cryptocurrency Autoview Trading Bot
---
### ESR-Bot: EMA Smoothed RSI Bot
![This is an image](https://github.com/Main-Michael-Sparks/ESR-Bot-/raw/main/ESRB%20Screenshots/ESRB.png)
---
> ***Requires Trading View and Autoview***

> Bot Created: 6/7/2021
##### Summery: How it works 
ESRB combines two technical indicators for buy and sell signals; it uses a slightly modified Relative Strength Index (RSI) and two Exponential Moving Averages (EMA). After a buy or sell signal is activated,  Autoview sends an order ticket to an exchange API for processing and execution. In other words, ESRB automatically trades cryptocurrencies based on its buy/sell signals. 

Thanks to Autoview and Trading View the bot operates directly in your browser as a Trading View chart overlay. 

##### Indicators

* Relative Strength Index (*[How RSI works](https://www.investopedia.com/terms/r/rsi.asp)*)
RSI generates buy and sell signals based on oversold or overbought conditions. 

![RSI Settings](https://github.com/Main-Michael-Sparks/ESR-Bot/raw/main/ESRB%20Screenshots/ESRB-Settings-1.png)

ESRB uses a traditional RSI with two modifications. The first is a user-defined (or deactivated) simple average of the RSI line itself. So, the RSI line can be smoothed to add more control over how it approaches the overbought and oversold lines. The second modification is an overbought range and an oversold range. Adding a "range" gives more control over what defines "overbought" and "oversold" within the context of RSI.  
*E.g Between 70%-80% can be defined as an overbought range or 20%-30% as an oversold range.*

* Long and Short Period Exponential Moving Averages (*[How MA crosses work](https://www.investopedia.com/articles/active-trading/052014/how-use-moving-average-buy-stocks.asp)*)
Long and short period EMAs generate buy and sell signals based on one crossing above or below the other. 

![EMA Settings](https://github.com/Main-Michael-Sparks/ESR-Bot/raw/main/ESRB%20Screenshots/ESRB-Settings-2.png)

ESRB uses two EMAs for cross detection and a search period to determine how long to apply a detected cross. 
*E.g.  If a 'Golden' cross or 'Death' cross appears then for the next 20 bars (10min|1hr|1day) create a buy or sell signal for the duration of those 20 bars.*

##### Trade Logic

A buy/sell signal is activated once the RSI line is in either overbought or oversold range, and the RSI line is also within an active EMA cross. *E.g. The RSI line is in the overbought range, and the RSI line is in a corresponding EMA cross('Death') period then a short trade signal is generated.*

##### Flip Trading Bot

ESRB is a flip (or switch) trading bot. Once the first trade is executed, the bot will keep switching directions based on its buy/sell signals. So if you start with a bullish trade, the bot stays in the bull trade until a bear/short signal is generated, at which point, the bot will exit the bull trade and enter the bear trade. (The ticket system includes a stop-loss to provide a kind of parashoot for worst-case scenarios.) In short, once the bot starts trading it will not stop until you tell it to. 

##### Ticket System

ESRB's ticket system is based on the options provided by Autoview. [Autoview's ticket options can be found here](https://autoview.with.pink/#syntax) *Note: Not all of Autoview's options are currently supported.*

![Long order settings](https://github.com/Main-Michael-Sparks/ESR-Bot/raw/main/ESRB%20Screenshots/ESRB-Settings-3.png)

ESRB currently supports buying and selling(shorting) at market price with or without leverage. ESRB also supports setting stop losses at a fixed price or as a percentage. Limit orders are currently not supported. 

![Short order settings](https://github.com/Main-Michael-Sparks/ESR-Bot/raw/main/ESRB%20Screenshots/ESRB-Settings-4.png)

Both sides of the trade ticket must be filled out for the flip trading mechanisms to work correctly. So the ticket for a bullish trade AND a ticket for a bearish trade must be filled out and ready to go before the bot starts trading.  

##### Exchanges with Built-in Support
* Gemini Sandbox:
A safe environment to test the bot.

* Kraken:
Untested in live accounts.

##### Trading Pairs with Built-in Support

*Crypto exchanges (API support) and Autoview have a limited number of trading pairs available. Autoview differs depending on the exchange's API support.*

ESRB-supported pairs are currently BTC/USD and ETH/USD.

>***NOT FINANCIAL ADVICE***

>*The settings on this bot are customizable to the point of insanity, and therefore, I am not responsible for any damage resulting from the use of this bot.*

>*Use of this bot or any part of this bot is NOT allowed unless you agree to the following:*
>1. You accept full responsibility for any damages resulting from the use of this bot.
>
>2. You have done your own research, and fully understand and accept the risks involved in the use of this bot, and any market that the bot is used with. 
>
>3. You have consulted with a financial professional about your financial situation, the use of this bot, and any markets that you plan on using the bot with or agree that you were advised to consult with a financial professional. 
>
>4. Nothing in this repository is specific financial advice, and I am not a financial advisor, accountant, or attorney. 



