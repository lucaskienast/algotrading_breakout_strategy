# Algotrading Breakout Strategy
In this project, I implemented a simple breakout strategy. I tested to see if it has the potential to be profitable using a Histogram and P-Value. For the dataset, I used the end of day from Quotemedia.

## Installation
Use `git clone` to get a copy of this repository.
```
$ git clone https://github.com/lucaskienast/algotrading_breakout_strategy.git
$ cd algotrading_breakout_strategy
```

## Method
- load market data
- create `dataframe` for close, high, and low prices
- compute highs and lows in period `lookback_days`
- compute long and short signals for _high<close_ and _low>close_
- filter the signals to remove consecutive equal signals within defined `lookahead_days`
- compute projected signal returns after `lookahead_days`
- use Kolgomorov-Smirnov Test to find stocks causing outlying returns

## Results
Found 24 outliers in the stock universe using Kolgomorov-Smirnov test. Signal returns moved closer to normal distribution after removing them.
