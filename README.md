
# Cryptocurrency Market Analysis Dashboard with Machine Learning Forecasting

## Project Overview

This project presents an interactive Cryptocurrency Market Analysis Dashboard developed using Power BI and Python. The dashboard integrates live cryptocurrency market data from the CoinGecko API to provide real-time insights into the performance of the top 100 cryptocurrencies by market capitalization.

The project combines Business Intelligence techniques with Machine Learning forecasting to enable both descriptive and predictive analysis. Users can explore market trends, compare cryptocurrency categories, identify top-performing assets, and analyze future Bitcoin price movements through a Linear Regression forecasting model.

---

## Project Objectives

The primary objectives of this project are:

* To collect and analyze live cryptocurrency market data.
* To develop an interactive Power BI dashboard for market visualization.
* To perform descriptive and comparative analysis of cryptocurrency performance.
* To implement a machine learning model for Bitcoin price forecasting.
* To demonstrate the integration of Python analytics within a Business Intelligence environment.

---

## Data Source

The project utilizes data obtained from the CoinGecko API, which provides near real-time cryptocurrency market information, including:

* Cryptocurrency Name and Symbol
* Current Price
* Market Capitalization
* Trading Volume
* Market Rank
* 24-Hour Price Change Percentage

Historical Bitcoin price data was also collected for predictive modeling purposes.

---

## Dashboard Features

### Market Overview

* Total Cryptocurrency Market Capitalization
* Average 24-Hour Price Change
* Total Number of Cryptocurrencies Analyzed
* Market Sentiment Indicators

### Cryptocurrency Analysis

* Top 10 Cryptocurrencies by Market Capitalization
* Top Gainers and Losers
* Market Capitalization Distribution
* Category-Based Comparison (Large Cap, Medium Cap, Small Cap)

### Interactive Filtering

* Dynamic Slicers
* Cryptocurrency Selection
* Category Filtering
* Search Functionality

### Forecasting Module

* Bitcoin Historical Price Trend
* Linear Regression Forecast
* Future Price Projection
* Forecast Accuracy Metrics

---

## Machine Learning Implementation

A Linear Regression model was developed using Python and Scikit-learn to forecast future Bitcoin prices.

### Model Workflow

1. Historical Bitcoin price data collection
2. Data preprocessing and feature engineering
3. Training and testing data split
4. Model training using Linear Regression
5. Model evaluation using:

   * Mean Absolute Error (MAE)
   * Root Mean Squared Error (RMSE)
   * R² Score
6. Future price forecasting

---

## Technologies Used

| Technology    | Purpose                             |
| ------------- | ----------------------------------- |
| Power BI      | Dashboard Development               |
| Python        | Data Processing and Forecasting     |
| Pandas        | Data Manipulation                   |
| NumPy         | Numerical Computation               |
| Scikit-learn  | Machine Learning                    |
| CoinGecko API | Data Collection                     |
| GitHub        | Version Control and Project Hosting |

---

## Repository Structure

```text
Cryptocurrency-Market-Analysis/
│
├── Cryptocurrency_Dashboard.pbix
├── Forecasting_Code.ipynb
├── Report.pdf
├── data/
│   ├── crypto_top100.csv
│   └── bitcoin_historical.csv
│
├── screenshots/
│   ├── dashboard_overview.png
│   ├── market_analysis.png
│   └── forecasting_results.png
│
└── README.md
```

## Key Insights

The analysis revealed that large-cap cryptocurrencies dominate the market, accounting for the majority of total market capitalization. Bitcoin and Ethereum continue to maintain significant influence over overall market trends. The forecasting model demonstrated the potential of integrating predictive analytics into Business Intelligence solutions for enhanced decision-making.

---

## Limitations

* CoinGecko provides near real-time rather than high-frequency trading data.
* The forecasting model is based on Linear Regression and assumes linear relationships.
* External factors such as news events and market sentiment were not incorporated.
* Forecasting was limited to Bitcoin historical data.

---

## Future Improvements

Future versions of this project may include:

* ARIMA Forecasting Models
* Facebook Prophet Forecasting
* LSTM Deep Learning Models
* Sentiment Analysis from Social Media
* Real-Time Streaming Data Integration
* Multi-Cryptocurrency Forecasting

---

## Author

**Umer Sajid**
MS Data Science
Pak-Austria Fachhochschule Institute of Applied Sciences and Technology

---

## License

This project was developed for academic and educational purposes.
