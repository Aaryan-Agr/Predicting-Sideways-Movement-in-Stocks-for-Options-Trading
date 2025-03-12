# Securities-Forecasting-Analysis
## This project is still under construction, I will update as I make progress on it [60%].
## Predicting Sideways Movement in Stocks for Options Trading  

## Overview  
This project analyzes S&P 500 stocks to determine the likelihood of sideways movement. Sideways movement is crucial for options trading strategies like iron condors, straddles, and strangles. The analysis is based on technical indicators such as:  

- **60-period Moving Average (MA_60)**  
- **Bollinger Bands (BB_High, BB_Mid, BB_Low)**  
- **Relative Strength Index (RSI_14)**  
- **MACD (12, 26, 9) and MACD Signal Line**  

The model calculates a **Normalized Difference** between MA_60 and MACD_Signal to determine potential stock movement trends within different GICS Sectors and Sub-Industries.

## Features  
- **Live Data Fetching:** Retrieves stock prices and indicators using Yahoo Finance.  
- **Sector and Sub-Industry Thresholding:** Computes statistical thresholds for sideways movement.  
- **Trend Classification:** Categorizes stocks into "Sideways Movement," "Upward Trend," or "Downward Trend."  
- **Earnings Impact Analysis:** Identifies the time to the next earnings report to avoid unexpected volatility.  

## Usage  
1. Run the script to fetch live stock data.  
2. Review the classification of stocks for sideways movement.  
3. Use the results to inform options trading strategies.  

## Next Steps  
- Improve model accuracy by incorporating volatility measures.  
- Extend the approach to non-S&P 500 stocks.  
- Develop a real-time dashboard for monitoring stock trends.  
