# Mean Reverting Strategy

*When I was researching in the ETF space, I found this interesting FANGMA index-based ETF listed on the Toronto Stock Exchange that is launched by Evolves and provided by Solactive AG. It is an equal weight index, so it's subject to rebalancing every once in a while. The FANGMA ETF contains 6 stocks: FB (META), AAPL, NFLX, GOOG, MSFT, AMZN. But I wanted to twist it with my own version and see if it has the potential to be profitable. In this research, I will apply a simple mean-reverting strategy on these stocks and backtest the strategy to see if it is lucrative.*

## 1. Scope of Research

We will cover the aforementioned 6 stocks over the span of the past 10 years.

## 2. Methodology

Instead of using equal weight approach like the ETF uses, I will apply daily mean reversion strategy, in which I will put more weight on the stock that is further from the average daily return and rebalance on a daily basis. Here are the steps:
- calculate the average equal-weighted portfolio daily return
- assign weights to each security based on their distance to the portfolio return
- select date of interest

## 3. Data Visualization

The chart below shows the daily % change of each stock.

![daily % change](https://github.com/hoytlui/Mean-Reverting-Quant-Research/blob/main/images/daily_percent_change.png)

## 4. Backtesting

We use two metrics for our backtesting
- Sharpe ratio
- Maximum drawdown

![Max drawdown](https://github.com/hoytlui/Mean-Reverting-Quant-Research/blob/main/images/cum_return.png)


## 5. Conclusion

- Sharpe ratio represents the risk-adjust return. For this strategy, it is negative even before any transaction costs, making this strategy unattractive
- Drawdown tells us how much the portfolio could have lost in the backtesting period. In this case, the maximum drawdown is 52.40% and has not been recouped for over 8 years
- This strategy is not proven to be profitable

## 6. Next Steps

To propose alternative methodologies, we can think about changing the allocation of the portfolio, looking for other securities, or using momentum instead of mean-reverting approach.
- Instead of finding weights based on their distance to the average return, we can apply technical or fundamental analysis such as RSI or P/E ratio to help us determine how much weights to put on each stock.
- As all stocks in the portfolio are in the large-cap Tech sector, we see that they tend to move in the same direction in the first graph => it may be better to use momentum strategy rather than mean-reverting strategy on their price movement.
- This leads to an alternative approach that perhaps the mean-reverting strategy fits better with inputs such as their daily return, as suggested in the graph that shows daily % change of each security.
