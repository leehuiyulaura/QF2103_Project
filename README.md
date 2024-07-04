# QF2103_Project: Research on Trading Strategies using Python
This project aims to provide a comprehensive analysis on the research on 2 different trading strategies, using Python as a computational tool, and explores the application of machine learning techniques to develop and enhance trading strategies. Specifically, this research focuses on two key strategies: local extrema identification and mean reversion analysis, both using logistic regression as the machine learning model.


The research aims to contribute to the field of quantitative finance by providing practical insights and methodologies for building effective trading strategies using machine learning techniques.


The stock data used can be obtained from the first five stocks in tr_eikon_eod_data.csv, named AAPL.O, MSFT.O, INTC.O, AMZN.O, and GS.N. The completed codes for this research can be found in Trading_Strategies_Analysis_Codes.ipynb, along with code-specific instructions and observations. This report is a detailed analysis on the application of the two strategies with the machine learning model.


## Local Extrema with Logistic Regression Model
Local min-max strategy, otherwise known as the local extrema trading strategy is a method used by traders to identify potential entry and exit points based on local highs (peaks) and lows (troughs) in price movements. This strategy aims to capitalise on short-term price fluctuations within a larger trend.


Average Base Profit: 2.797
Average Annualized Return: 1.194


We achieved satisfactory returns and profits on our base local extrema trading strategy model as evidenced by the high returns and base profit. Of the 5 stocks, AMZN.O generated the best results, with a base profit os 4.8227 and annualized return of 1.822. Conversely, AAPL.O returned the smallest profits, a considerable 1.805 and an annualized return of 0.8352. This could be attributed to the volatility of the stocks, as the AAPL.O stocks have an annualized volatility of 0.14154, which is low compared to AMZN.O. The model's buy and sell points suggest fewer significant price swings to capitalize on, which may result in lower profits. In contrast, the AMZN.O chart shows a stronger upward trend with more pronounced fluctuations, which are opportunities for a trading model to generate profits. The annualized volatility is 0.181761, slightly higher than AAPL.O, which may indicate more price movement to exploit. In addition, AAPL.O’s Sharpe ratio of 5.901196 indicates a decent risk-adjusted return, but the Calmar ratio of 13.719754, while high, suggests the risk-adjusted returns over the maximum drawdown period were not as strong as AMZN.O. In contrast, the Sharpe ratio of AMZN.O is extremely high at 10.021932, indicating that the excess return per unit of risk is very favorable. The Calmar ratio is also outstanding at 23.445381, suggesting a very strong performance relative to the maximum drawdown.


Therefore, from the trends observed in the stock charts, we concluded that our machine learning model used may be better suited to stocks like AMZN.O, which show more pronounced trends and volatility. Since the model is based on local extrema trading strategy, stocks with clear local minima and maxima for the model to trade on offer more opportunities for the model to make profitable trades


## Mean Reversion with Logistic Regression Model
Mean reversion is a financial theory suggesting that asset prices and returns tend to move back towards their long-term mean over time. The mean reversion trading strategy is based on the idea that when the price of an asset deviates significantly from its historical average, it is likely to revert back to the mean. It aims to identify assets that are significantly overvalued or undervalued and take positions based on the expectations that it will revert back to the mean.


The mean reversion machine learning model performs better than the raw mean reversion on the MSFT.O, AAPL.O, AMZN.O and GS.N test data. The outlier being the INTC.O test data where the raw mean reversion performed better than the mean reversion machine learning model. This could be attributed to the fact that the INTC.O train data has relatively sharp downwards price trends. 


From our results, the average base profit from the mean reversion machine learning model is +24.39%, 1.2% better than the standard mean reversion model. Overall, the mean reversion machine learning model outperformed the raw mean reversion on the test data, with a higher annualised return at +14.30%, lower annualised volatility and max drawdown at 13.16% and - 10.52% respectively indicating that the model has lower volatility and risk, higher Sharpe ratio at 1.13 and higher Calmar ratio at 1.61 thus suggesting that it generates higher risk-adjusted returns. 


On the other hand, the average accuracy of the model, which is defined to be the proportion of correct prediction (for both true positives and true negatives) among the total number of predictions is 88.90%


## Comparison of both strategies
Comparing between the basic models of local extrema trading strategy and the mean reversion trading strategy we noticed that the local extrema trading strategy was able to generate much greater profits across all 5 stocks , about 3.28 times more than the mean reversion trading strategy.


## Conclusion
In conclusion, from the differing performance on accuracy and profit on both strategies depending on which stock is used to train the model, we learnt that different stocks exhibit unique patterns and behaviours, requiring tailored strategies. The performance variation across different stocks indicates that a one-size-fits-all approach may not be optimal. 
