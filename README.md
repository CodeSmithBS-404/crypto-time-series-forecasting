# Crypto Forecasting — Time Series Forecasting

A Python/Jupyter Notebook project for analyzing cryptocurrency price data and building time-series forecasting models. The notebook downloads the latest available historical cryptocurrency data at runtime and compares multiple forecasting approaches.

## Project Overview

This project uses historical cryptocurrency market data to:

- Download the latest available cryptocurrency price data
- Perform exploratory data analysis (EDA)
- Analyze daily returns and volatility
- Create technical/time-series features
- Train and compare multiple forecasting models
- Evaluate model performance using standard regression metrics
- Generate a 30-day recursive forecast using an LSTM model

The default cryptocurrency is **Bitcoin (BTC-USD)**, but the notebook can be configured for other supported symbols such as Ethereum, Solana, and BNB.

## Models Used

The notebook includes the following models:

1. **Naive Forecast**
   - Uses the most recent observed value as the prediction.
   - Serves as a simple baseline.

2. **ARIMA**
   - Statistical time-series model.
   - Configured in the notebook as ARIMA(5, 1, 0).

3. **Prophet**
   - Designed for time-series forecasting with trend and seasonality components.

4. **Random Forest**
   - Machine-learning regression model using lagged prices and technical indicators.

5. **LSTM**
   - Long Short-Term Memory neural network.
   - Used for sequential time-series forecasting and future prediction.

## Features

The notebook creates several features from the historical price data, including:

- Lagged closing prices
- Simple Moving Average (SMA)
- Exponential Moving Average (EMA)
- MACD
- Rolling volatility
- RSI
- Daily returns

These features are used to help the machine-learning models identify patterns in historical market data.

## Evaluation Metrics

The models are evaluated using:

- **MAE (Mean Absolute Error)** — average absolute prediction error.
- **RMSE (Root Mean Squared Error)** — penalizes larger errors more strongly.
- **MAPE (Mean Absolute Percentage Error)** — expresses prediction error as a percentage.

The notebook also produces comparison plots to make the model results easier to analyze.

## Data Source

Historical cryptocurrency data is downloaded using the **Yahoo Finance** data service through the `yfinance` Python package.

The data is fetched when the notebook is executed, so the project does not rely on a permanently stored historical dataset.

Default ticker:

```text
BTC-USD
```

Example alternative tickers:

```text
ETH-USD
SOL-USD
BNB-USD
```

## Requirements

The project uses Python and Jupyter Notebook.

Required Python packages:

```text
yfinance
pandas
numpy
matplotlib
seaborn
scikit-learn
statsmodels
prophet
tensorflow
ta
```

You can install all dependencies with:

```bash
pip install yfinance pandas numpy matplotlib seaborn scikit-learn statsmodels prophet tensorflow ta
```

The notebook also contains an installation cell, so the dependencies can be installed directly from Jupyter.

## How to Run

### 1. Open a terminal

On Windows PowerShell or Command Prompt, verify Python:

```bash
python --version
```

### 2. Start Jupyter Notebook

```bash
jupyter notebook
```

### 3. Open the notebook

Open:

```text
Crypto_Forecasting_Time_Series_Forecasting.ipynb
```

### 4. Run the notebook

In Jupyter:

**Kernel → Restart Kernel and Run All**

The notebook will:

1. Load the required libraries.
2. Download the latest cryptocurrency data.
3. Perform exploratory analysis.
4. Generate forecasting features.
5. Train the forecasting models.
6. Evaluate the models.
7. Compare their predictions.
8. Generate a 30-day future forecast using the LSTM model.

## Changing the Cryptocurrency

The notebook contains a ticker configuration variable.

For example:

```python
TICKER = "BTC-USD"
```

You can change it to:

```python
TICKER = "ETH-USD"
```

or:

```python
TICKER = "SOL-USD"
```

After changing the ticker, restart and run the notebook again.

## Project Structure

```text
Crypto Forecasting/
│
├── Crypto_Forecasting_Time_Series_Forecasting.ipynb
└── README.md
```

## Important Notes

- Cryptocurrency prices are highly volatile.
- Historical patterns do not guarantee future performance.
- Forecasting models can produce inaccurate predictions, especially during sudden market movements.
- The forecast is intended for educational and research purposes.
- This project is **not financial advice**.
- An internet connection is required when downloading fresh data from Yahoo Finance.

## Expected Output

When the notebook runs successfully, it produces:

- Cryptocurrency price charts
- Daily return and volatility analysis
- Technical indicator visualizations
- Train/test datasets
- Model predictions
- Model performance metrics
- Actual-vs-predicted comparison plots
- A model comparison table
- A 30-day future LSTM forecast

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Statsmodels
- Prophet
- TensorFlow / Keras
- TA
- yfinance

## Disclaimer

This project is intended for **educational purposes only**. Cryptocurrency forecasting is inherently uncertain, and model predictions should not be treated as guaranteed future prices or financial recommendations.
