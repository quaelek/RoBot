# RoBot: RobinhoodBot v2

To Install:

```bash
git clone https://github.com/2018kguo/RobinhoodBot.git](https://github.com/quaelek/RoBot.git
cd RoBot
pip install -r requirements.txt
cp config.py.sample -> config.py # add auth info after copying
```

To Run:

```python
cd RobinboodBot/robinhoodbot (If outside of root directory)
python3 main.py
```

## RobinhoodBot [Original ReadMe]
Trading bot for Robinhood accounts

For more info:
https://medium.com/@kev.guo123/building-a-robinhood-stock-trading-bot-8ee1b040ec6a

5/1/19: Since Robinhood has updated it's API, you now have to enter a 2 factor authentication code whenever you run the script. To do this, go to the Robinhood mobile app and enable two factor authentication in your settings. You will now receive an SMS code when you run the script, which you have to enter into the script.

2/23/21: Check out this documentation page for a possible workaround
https://github.com/jmfernandes/robin_stocks/blob/master/Robinhood.rst

This project supports Python 3.7+

## Trading Strategy - Overview

This is a simple trading strategy that uses two moving averages, a short-term indicator and a long-term indicator, to detect when to buy and sell a stock. The strategy is implemented in Python code that can be run on historical data to see how well it performs.

The strategy loads data from a CSV file containing the closing prices of the stock being traded, and filters the data to start at a specified date. It then calculates the moving averages and uses them to determine when to buy and sell the stock.

If the short-term moving average crosses above the long-term moving average, the strategy buys the stock. If the short-term moving average crosses below the long-term moving average, the strategy sells the stock. The strategy also includes parameters for stop loss, take profit, and trailing stop, which are used to limit losses and lock in profits.

## Designed for Volatile Assets
  
This strategy can perform well on volatile assets because it uses a combination of short-term and long-term moving averages to detect trends and make trading decisions. Volatile assets tend to have rapid price movements and sudden changes in direction, which can make it difficult to predict the future direction of the price.

By using both short-term and long-term moving averages, this strategy can help filter out some of the noise in the price data and identify the underlying trend. The short-term moving average can react quickly to changes in the price, while the long-term moving average can provide a broader perspective on the direction of the trend.

## Backtesting

Adding backtesting allows you to test how well your strategy would perform on historical data, and to identify the best set of parameters for a given asset. By simulating trades using past data, you can see how the strategy would have performed under different market conditions and identify any weaknesses or opportunities for improvement.

_Backtesting results are not indicative future returns._

Additionally, you can run testparameters.py with the backtesting to see the portfolio's performance over time; what if for the parameters you have, all of the growth happened entirely within the last 10% of the fund's lifespan and for the remainder of the time it was _under_?
_
