# Time Series Analysis - Yen

The purpose of this analysis it to analyze the current trends of the Japanese Yen futures in terms of a time-series analysis.  

## ARMA, ARIMA, & GARCH

### Actual Settlements v. Trends

![Settlement v. Trend](images/Settle_v_Trend.png)

 - Plotting the historical data reveals some variance around the trend which may present trading opportunities.  Overall, there is an increasing trend in the value of the Yen compared to the USD.

### ARMA Model Forecast

![ARMA Forecast](images/ARMA_Yield_Forecast.png)

![ARMA Results](images/ARMA_Results.png)

 - The ARMA model does not appear to be a good fit to forecast the data given the P-Value is greater than 0.05 for each lag test.  The high AIC and BIC values also support this.

 ### ARIMA Forecast

![ARIMA Forecast](images/ARIMA_Yield_Forecast.png)

![ARMA Results](images/ARIMA_Results.png)

 - The ARIMA model shows an anticipated increase in the value of the Yen; however, given the P value results are greater than 0.05x the model does not appear to be good fit for the data. 

 ### GARCH Volatility Forecast

![GARCH Forecast](images/GARCH_Forecast.png)

 ![GARCH Results](images/GARCH_Results.png)

  - The GARCH model indicates future volatility in the Yen over the 5 day horizon.
  - GARCH model is a more statistically significant model based on the data because the P value is less than 0.05 based on the lag calculations.

### ARMA, ARIMA, GARCH Conclusion

 - The models forcast continued upward trend of the Yen against the USD; however, the ARMA and ARIMA models are not good fit for the data given the high P-Values.  The GARCH model is the best fit for the data given the acceptable P-Value calculations less than 0.05.  
 - I would not recommend a trading decision based on the ARMA and ARIMA models given the lack of fit; however, the model parameters could be tuned to better fit the data which is outside the scope of this assignment.  

 ## Linear Regression

![Best Fit Line](images/Best_Fit_Line_LR.png)

 ![Return v. Predicted Return](images/Return_Predicted_Return_Plot.png)

  - Out-of-Sample Root Mean Squared Error (RMSE): 0.41521675083603804
  - In-sample Root Mean Squared Error (RMSE): 0.5658708047560468

 - The Linear Regression model performs better on in sample data than out of sample data when reviewing the RMSE.  The out of sample test has an RMSE of 0.41 which is lower compared to
the in sample test which has a value of 0.56.  The lower RMSE indicates higher accuracy.  