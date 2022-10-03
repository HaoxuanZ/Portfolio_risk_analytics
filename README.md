# Volatility Trading Strategies using VIX and Gold
**Volatility Trading Strategies using VIX and Gold.**

**Haoxuan Zhang**

**Introduction:**

For this project, the goal is to find out the performance of US Equity, Gold, and VIX during different periods. We want to figure out between Gold and VIX, which one is a better hedge for US Equity. To conduct the analysis, we used data from 01/01/2007 until 03/31/2020. S&P 500 (Ticker: \^GSPC) and Nasdaq (Ticker: \^IXIC) was chosen to represent the US Equity. Gold (Ticker: GLD) and VIX (Ticker: \^VIX) data is also collected for the project.

For this project, we focused on three periods:

    -   2007-2009 Bear market (01/01/2007 to 03/31/2009)
    -   2009-2020 Bull market (03/31/2009 to 01/31/2020)
    -   Covid-19 Pandemic (02/01/2020 to 03/31/2020)
**Performance of each asset:**

To begin with, we will take a look at the cumulative performance of the S&P 500, Nasdaq, and Gold for the period from 01/01/2007 to 03/31/2020.

![](https://github.com/HaoxuanZ/portfolio_risk_analytics/blob/master/SP500_performance.png)

Graph 1: Cumulative performance of S&P 500, Nasdaq, and Gold, from 01/01/2007 to 03/31/2020.

From the graph1, we can see that Nasdaq achieved the best performance among the three since it had the highest cumulative return of 220.8%, from the beginning of 2007 to the end of March of 2020. Gold reached the second-highest cumulative return of 145.5% and the S&P 500 had the lowest cumulative return of 85.4%.

![](https://github.com/HaoxuanZ/portfolio_risk_analytics/blob/master/performance_0720.png)

Graph 2: Cumulative performance of S&P 500, Nasdaq, and Gold, from 01/01/2007 to 03/31/2009.

From Graph 2,during the Global Financial Crisis, Gold which relies on it unique financial attribute achieved the highest cumulative return of 44.5%. Nevertheless, both the S&P 500 and Nasdaq had losses because of the crisis. S&P500 lost 44.4% of its value and Nasdaq lost 38.0% of its value. Therefore, we can see that both equity indexes suffered from the crisis. However, Gold managed to hedge the risk of the poor performance of the stock market.

![](https://github.com/HaoxuanZ/portfolio_risk_analytics/blob/master/performance_09-20.png)

Graph 3: Cumulative performance of S&P500, Nasdaq, and Gold, from 03/31/2009 to 01/31/2020.

2009 - 2020 is the best year of American market. This historical long term bull market leads American economy to climax. We can see Nasdaq reaches its very best cumulative performance. It has the highest cumulative return which is 498.7%. S&P500 also reached to 304.3% cumulative return. However, gold market only had a flat performance which demonstrated it special financial attribute to the Nasdaq and S&P500.

![](https://github.com/HaoxuanZ/portfolio_risk_analytics/blob/master/performance_20-20.png)

Graph 4: Cumulative performance of S&P500, Nasdaq, and Gold, from 02/01/2020 to 03/31/2020.

Finally, due to the Covid-19 pandemic, both Nasdaq and S&P 500 plunged in February and March. Nasdaq lost 16.2% of its value and S&P 500 lost 19.2% of its value. The performance of Gold was relatively more stable than the other two, ending up with a return of 3.1%.

**Correlation analysis:**

To identify which one is a better hedge between Gold and VIX, we need to figure out the correlation of each possible asset pair during different time periods.

![](https://github.com/HaoxuanZ/portfolio_risk_analytics/blob/master/overall_correlation.png)

Graph 5: Overall Correlation of each asset.

In the overall time that between 2007 to 2020, the correlation between Nasdaq and VIX is always strongly negative correlated. Also as S&P 500 and VIX. In the previous analysis we said that Gold seems had opposite linear relation with US equity. However, in our new analysis we can clearly see the correlation of Gold to Nasdaq and S&P 500 vibrated between positive and negative. Moreover, the correlations are not as strong as VIX to US equities. Thus, in the overall time period. VIX is a better hedge than gold.

![](https://github.com/HaoxuanZ/portfolio_risk_analytics/blob/master/bear_correlation.png)

Graph 6: Bear Market.

Throughout the Financial Crisis, the correlations of Gold to US equities went to negative from positive. However the correlations are not strong and stable for hedge strategy. Back to VIX, it keeps the highly negative correlation to US equities even through the crisis. This attribute can help portfolio manager mitigate their lost.

![](https://github.com/HaoxuanZ/portfolio_risk_analytics/blob/master/bull_correlation.png)

Graph 7:Bull Market.

During the Bull Market that lasted from 2009 to 2020, we had the same conclusion as in the Financial Crisis, which is that VIX was a better hedge than Gold. The correlations between VIX and US equities remained negative during the decade.

![](https://github.com/HaoxuanZ/portfolio_risk_analytics/blob/master/covid_correlation.png)

Graph 8: Pairwise correlation plots from February of 2020 to March of 2020.

Due to the recent pandemic, the American stock market suffered a huge plummet. 5 times circuit breakers melted billions of dollars in the market. But still, the strong negative correlation between VIX and US equities can help us to minimize lost by hedge strategy.

**Beta analysis:**

Besides correlation, beta is another significant factor that we need to think about when finding a better hedge. Correlation shows the strength of a linear relationship between two assets. Beta tells us the magnitude of one asset’s change given how much the other asset varies.

|          | Beta of Gold | Beta of VIX | R-squared of Gold | R-squared of VIX |
|----------|--------------|-------------|-------------------|------------------|
| 07-20    | 0.02301      | -4.54933    | 0.001             | 0.518            |
| 07-09    | 0.02162      | -3.0319     | 0.001             | 0.563            |
| 09-20    | 0.01101      | -6.49406    | 0.000             | 0.601            |
| Covid-19 | 0.07469      | -2.82554    | 0.033             | 0.569            |

Table 1: Summary table of beta and r-squared for different time periods.

From the table, we can see that the beta of Gold is close to 0, no matter in which period. Also, the r-squared is extremely low, indicating that the linear regression model explains little variability of the data. However, VIX’s beta remains negative for any time, which tells that when the S&P 500 drops, the return will increase for VIX. Thus, VIX will be a better hedge than Gold. In addition, the r-squared for VIX is around 0.6, showing that the model can explain 60% of the variability of the data.

|          | Correlation of predicted value vs actual value for GLD | Correlation of predicted value vs actual value for VIX |
|----------|--------------------------------------------------------|--------------------------------------------------------|
| 07-20    | 0.026233                                               | 0.719392                                               |
| 07-09    | 0.026478                                               | 0.75047                                                |
| 09-20    | 0.010711                                               | 0.775281                                               |
| Covid-19 | 0.182182                                               | 0.754392                                               |

Table 2: Summary table of correlations between predicted values and actual values.

We also utilized each model to predict the performance of assets and find out the correlations between the prediction and actual data. From the table, we notice that for each period, the correlation for GLD is significantly lower than the correlation for VIX. This tells us that VIX’s models are much better in predicting values than GLD’s models, which supports the conclusion that VIX is a better hedge than Gold.

**VIX Hedge Test**

Since we find out VIX is a better hedge than Gold. Now we apply our strategy into a portfolio experiment to test if our strategy can help us to minimize our lost and maximize our returns.

In Graph 9, the difference between no-strategy trading and VIX hedge trading is huge.The portfolio follows the Volatility Trading Strategy. we test the real 21 standard deviation and compare those data with VIX in 1 month back. Then, when it is low volatility regime, the portfolio allocation was 100% in S&P500. Since real standard deviation less then VIX +2% which mean market real volatility had not reach the predicted volatility.In contrast, the equity allocation reassigned to 40% in S&P500,60% in VIX. Since market had higher volatility than prediction. Within the strategy, we once had the 11.9% cumulative return. But with no strategy, the highest point was 1.34%.

![](https://github.com/HaoxuanZ/portfolio_risk_analytics/blob/master/Portfolio_performance.png)

Graph 9: Cumulative performance plots for our portfolio and S&P 500.

|                        | Portfolio | S&P 500  |
|------------------------|-----------|----------|
| Annualized return      | 19.89%    | 4.65%    |
| Annualized volatility  | 45.39%    | 20.73%   |
| Sharpe ratio           | 0.44      | 0.22     |
| Maximum drawdown       | 40.0808%  | 52.5785% |
| VaR-daily(95)          | -2.7262%  | -1.9785% |
| CVaR(95%)              | -5.4516%  | -4.2196% |

Table 3: Summary table of returns, volatility and other information for portfolio and S&P 500.

From the table, we can see that our portfolio has a higher return of 19.89% per year with a higher volatility of 45.39% per year. By comparison, investing only in the S&P 500 can bring a return of 4.65% per year with a lower volatility of 20.73% per year. Our goal is to select the option with a higher Sharpe ratio. We notice that our strategy generates a Sharpe ratio of 0.44, but S&P 500 only has a Sharpe ratio of 0.22. This means that our strategy can produce a higher return per unit of risk.

In addition, the portfolio has a lower maximum drawdown of 40.0808% than 52.5785% of the S&P 500. It indicates that our strategy had a maximum loss of 40.0808% of its value. However, for our strategy, 5% of the time the minimum daily loss is -2.7262%, where the S&P 500 only has a loss of -1.9785%. What is more, the expected loss in the worst 5% of scenarios for the portfolio is -5.4516%. S&P 500 has a lower expected loss in the worst 5% of scenarios of -4.2196%. Although our strategy has a higher risk, it can generate more return per unit of risk. Therefore, our strategy outperforms the S&P 500.

**Conclusion:**

From previous parts, VIX is a better hedge for the US stock market, no matter in the bull market or in the bear market. This result can be proved by the strong negative correlation, the correlation of Gold to US equities fluctuates between positive and negative, Gold will not be a good choice for a hedge. In addition, from the test result of using VIX as a hedge, we found out our strategy can generate a higher return per unit of risk than the S&P 500. This finding also validates that VIX is a good hedge. In summary, the VIX is a better hedge during the bear market of US stocks.

**Appendix**:

|          | Percentage of the time that the price of S&P 500 is above its moving average  |
|----------|-------------------------------------------------------------------------------|
| 07-20    | 70.81%                                                                        |
| 07-09    | 7.45%                                                                         |
| 09-20    | 78.96%                                                                        |
| Covid-19 | 26.74%                                                                        |

Table 4: Summary table of the relationship of price of S&P 500 and its moving average.

During the Great Recession, 7.45% of the time the price of S&P 500 is above its moving average. This means that the price was dropping in the majority of the time.   
 During the Bull Market, 78.96% of the time the price of S&P 500 is above its moving average. When the price is higher than the moving average, we will get a higher moving average for the later period. Therefore, during the Bull Market, the price of S&P 500 was increasing in the most of the time.

From the March of 2019 to the end of March of 2020, 26.74% of the time the price of S&P 500 is above its moving average. This is similar to the economic depression of 2008, where the price was decreasing.

For the whole period that lasted from 2007 to March of 2020, 70.81% of the time the price of S&P 500 is above its moving average. This indicates that despite of the Great Recession and current Covid-19 pandemic, the overall performance of US stocks is good.


 
