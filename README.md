# Securities-Forecasting-Analysis
## Predicting Sideways Movement in Stocks for Options Trading  


## **Overview**

This project uses machine learning to predict the price movement of stocks in the S&P 500 index, focusing on identifying stocks that are likely to show **sideways movement**. The key idea is that stocks that exhibit a sideways trend are ideal candidates for **options trading strategies** like **straddles** and **strangles**, where both calls and puts are bought on the same stock, allowing for profits with low capital investment.

This project utilizes various **technical analysis** indicators such as **Moving Averages (MA)**, **Bollinger Bands (BB)**, **RSI**, and **MACD** to determine stock movement patterns and predicts whether a stock will exhibit **upward**, **downward**, or **sideways** trends.

### **Why Sideways Movement for Options?**

In options trading, a **sideways movement** strategy can be particularly advantageous because:

1. **Low Capital Investment**: By buying both call and put options, traders can profit from price movements in either direction.
2. **Limited Risk**: The maximum risk is limited to the cost of the options (premium), which makes it suitable for low capital trading.
3. **High Profit Potential**: If the stock moves sharply in either direction, the gains from one of the options (call or put) can offset the cost of both options and lead to substantial profits.

## **Features**

- **Data Collection**: The project fetches real-time stock data and calculates key technical analysis indicators for each stock in the S&P 500.
- **Trend Prediction**: The model predicts whether a stock will show an **upward**, **downward**, or **sideways** trend based on the calculated indicators.
- **Classification Models**: The predictions are made using **Logistic Regression**, **Support Vector Machines (SVM)**, and **Random Forest** models, which are trained on past stock performance data.
- **Earnings Date Filter**: The model takes into account upcoming earnings reports to avoid periods of high volatility that might skew predictions.
- **Thresholds by Sector/Sub-Industry**: The model uses industry-specific thresholds to enhance predictions for stocks in the same sector or sub-industry.

## **Libraries Used**

- `yfinance`: To download historical stock data.
- `pandas`: For data manipulation and analysis.
- `ta`: To calculate technical analysis indicators like **Bollinger Bands**, **RSI**, and **MACD**.
- `scikit-learn`: For machine learning models and metrics.
- `matplotlib`, `seaborn`: For data visualization.
- `joblib`: To save and load the trained models.

## **Getting Started**

### **Installation**

To get started with the project, you can clone this repository and install the required dependencies.

1. Clone the repository:
git clone https://github.com/Aaryan-Agr/sideways-stock-predictor.git cd sideways-stock-predictor

2. Install dependendencies
pip install -r requirements.txt

3. Run the code


### **Usage**

- **Step 1: Fetch Data**: The code fetches stock data for all S&P 500 companies for the past 6 months and calculates key technical indicators.
- **Step 2: Data Preprocessing**: It preprocesses the data by normalizing the difference between **MA_60** and **MACD_Signal**, calculates trend predictions, and adds earnings date filters.
- **Step 3: Model Training**: Using machine learning models like **Logistic Regression**, **SVM**, and **Random Forest**, the project trains and tests the models on the data to predict if a stock will trend sideways, upward, or downward.
- **Step 4: Model Evaluation**: The models are evaluated using accuracy, precision, recall, F1 score, and ROC curves.
- **Step 5: Saving the Model**: The trained **SVM** model and **scaler** are saved using `joblib` to allow for future predictions on new data.

### **Code Example**

To fetch data for a specific stock (e.g., 'AAPL') and check if it is likely to move sideways: (Feature to be implemented)

```python
ticker = 'AAPL'
stock_df = get_stock_data(ticker)

# If successfully retrieved data
if stock_df is not None:
 print(stock_df)
```


### **Future Enhancements**

- Integrate real-time stock data for continuous predictions.
- Develop a portfolio management system for automated options trading based on predictions.
- Use deep learning models (e.g., LSTM) for time-series prediction to further enhance accuracy.
- Add a Options Visualizer to understnad profit and loss margins.

Conclusion
This project provides a tool to identify stocks in the S&P 500 that are likely to move sideways, making them ideal candidates for options trading strategies with low capital investment. With the help of machine learning and technical analysis, traders can use this tool to enhance their options trading strategies and increase the chances of profitability.
