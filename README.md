# Algotrading Breakout Strategy
This is a simple breakout algotrading strategy written in Python. It works as follows:
- load market data
- create `dataframe` for close, high, and low prices
- compute highs and lows in period `lookback_days`
- compute long and short signals for _high<close_ and _low>close_
- filter the signals to remove consecutive equal signals within defined `lookahead_days`
- compute projected signal returns after `lookahead_days`
- use Kolgomorov-Smirnov Test to find stocks causing outlying returns
