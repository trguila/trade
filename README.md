# Ninjatrader
Strategy Website
This is a NinjaTrader strategy called `LazyRiverStrategy`. It's a scalping strategy that operates on a 5-minute timeframe and uses the 20-period and 50-period Exponential Moving Averages (EMAs). Here's a high-level overview of what it does:

1. **Initialization**: The strategy initializes several technical indicators, including two EMAs, the Relative Strength Index (RSI), Chaikin Money Flow (CMF), Average Directional Index (ADX), and Pivots. It also sets the profit target and stop loss levels.

2. **Long Entry Condition (Set 1)**: The strategy enters a long position when the following conditions are met:
    - The close price is greater than both the 50-period EMA (7 bars ago) and the 20-period EMA (2 bars ago).
    - The 20-period EMA is above the 50-period EMA.
    - The low of the current bar is equal to or higher than the 20-period EMA.
    - The close price 3 bars ago was above the 50-period EMA.
    - The RSI is less than 70.
    - The CMF is positive.
    - The ADX is above 25.
    - The close price is above the pivot point.

3. **Short Entry Condition (Set 2)**: The strategy enters a short position when the following conditions are met:
    - The close price is less than both the 50-period EMA (7 bars ago) and the 20-period EMA (2 bars ago).
    - The 20-period EMA is below the 50-period EMA.
    - The high of the current bar is equal to or lower than the 20-period EMA.
    - The close price 3 bars ago was below the 50-period EMA.
    - The RSI is above 30.
    - The CMF is negative.
    - The ADX is above 25.
    - The close price is below the pivot point.

Please note that this is a simplified explanation. The actual trading logic might be more complex and involve additional conditions or checks. Always thoroughly backtest any trading strategy before live trading.

If you have any ideas how to improve the strategy please let me know?
