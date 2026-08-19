# Cryptocurrency Market Analysis with Power BI and Linear Regression

This repository contains an academic cryptocurrency market-analysis project that combines a **Power BI dashboard** with a **Google Colab/Jupyter forecasting notebook**. The work covers descriptive market analysis, top-asset comparisons, Bitcoin historical-price processing, and a simple Linear Regression experiment that produces an iterative 30-day forecast.

The project is best presented as an educational analytics study and a portfolio example of combining business intelligence with introductory time-series feature engineering. It is **not** a live trading system, investment recommendation, or production-grade price-prediction service.

## What is actually included

| Artifact | Role |
| --- | --- |
| `Forcasting_code.ipynb` | Colab-compatible notebook that calls CoinGecko endpoints, saves market snapshots, builds Bitcoin time features and a lagged-price feature, evaluates Linear Regression, and writes forecast output. The filename is retained from the original project. |
| `task 3.pbix` | Power BI report file for the dashboard and interactive market-analysis views. Open with Power BI Desktop. |
| `historical.csv` | Bundled Bitcoin historical-price snapshot used by the notebook. |
| `forecast (1).csv` | Bundled forecast export from the notebook workflow. |
| `TASK3 &4 REPORT.docx` | Academic report accompanying the dashboard and forecasting work. |
| `requirements.txt` | Minimal Python environment for the notebook workflow. |

## Notebook workflow

The notebook contains the following stages:

1. Calls the CoinGecko markets endpoint to retrieve a top-100 market snapshot and writes `crypto_top100.csv`.
2. Calls the CoinGecko Bitcoin market-chart endpoint for approximately 90 days of historical prices and writes `historical.csv`.
3. Creates `TimeInSeconds` and `Price_Lag1` features.
4. Uses an ordered 80/20 train/test split rather than a random shuffle.
5. Fits a scikit-learn `LinearRegression` model and reports MAE, RMSE, and R².
6. Iteratively generates 30 days of hourly forecast points and writes `forecast.csv`.
7. Includes an additional exploratory cell that creates a volatility-shaped forecast export; this should be treated as an experiment, not as an independently validated model.

The recorded notebook output reports **MAE 179.95, RMSE 261.49, and R² 0.9847** for its saved historical test split. These are results from the bundled notebook run and should not be interpreted as evidence of reliable future-market performance. A lagged-price feature and a short historical window can make an in-sample or near-term backtest appear strong while still failing under market regime changes.

## Reproduce the Python workflow

Create an environment and install the notebook dependencies:

```bash
git clone https://github.com/UmerSajid842/cryptocurrency-market-analysis.git
cd cryptocurrency-market-analysis
python -m venv .venv

# macOS/Linux
source .venv/bin/activate

# Windows PowerShell
# .venv\Scripts\Activate.ps1

pip install -r requirements.txt
jupyter notebook Forcasting_code.ipynb
```

Run the notebook cells in order. The CoinGecko API calls require network access and may be rate-limited or return data that differs from the bundled snapshots. For a fully offline review, use the tracked CSV files and inspect the existing notebook outputs.

## Open the Power BI dashboard

Open `task 3.pbix` in Power BI Desktop. The PBIX file is the primary dashboard artifact in this repository. The current repository does not include a live web dashboard, a Streamlit app, or a screenshot directory; those are intentionally not claimed here.

The report and notebook were developed for academic/educational analysis. Refreshing the report may require reconnecting its data sources in Power BI and adapting the data model to the local CSV or a newly collected market snapshot.

## Data source

The notebook uses public CoinGecko API endpoints for market and Bitcoin historical-price data. The repository also includes dated CSV snapshots so that reviewers can inspect the project without making an API request. API responses, asset rankings, and prices change over time; the committed snapshots should be treated as historical project artifacts rather than current market data.

## Limitations and responsible use

Cryptocurrency markets are volatile, non-stationary, and affected by factors not represented in this notebook, including liquidity, market structure, news, regulation, sentiment, and macroeconomic conditions. The Linear Regression model uses a small feature set and does not establish causality. The evaluation is a single chronological split and is not a walk-forward backtest with transaction costs, slippage, uncertainty intervals, or a live monitoring process.

Accordingly, the forecast should not be used by itself to buy, sell, or hold any asset. This repository demonstrates an analytics workflow and its limitations; it does not provide financial advice or a reliable basis for investment decisions.

## Portfolio positioning

This project demonstrates **Power BI reporting, API-backed data collection, Pandas feature engineering, chronological model evaluation, and transparent communication of forecasting limitations**. It complements the applied ML and data-product work on the [Umer Sajid GitHub profile](https://github.com/UmerSajid842) and the [active portfolio](https://umer-portfolio-preview.vercel.app/).

## References

1. [CoinGecko API documentation](https://docs.coingecko.com/)
2. [CoinGecko Markets API endpoint used in the notebook](https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&order=market_cap_desc&per_page=100&page=1&sparkline=false)
3. [CoinGecko Bitcoin market-chart endpoint used in the notebook](https://api.coingecko.com/api/v3/coins/bitcoin/market_chart?vs_currency=usd&days=90)
4. [Cryptocurrency Market Analysis repository](https://github.com/UmerSajid842/cryptocurrency-market-analysis)
