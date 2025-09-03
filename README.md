# Financial Risk Analysis and Modeling (FRAM)

This project performs financial risk analysis and modeling using historical stock market data. It leverages **R** packages in a Jupyter Notebook to fetch market data, perform regression, stationarity tests, ARIMA forecasting, and GARCH modeling.

## Features

- **Data Acquisition**  
  Fetches historical price data for:
  - Nifty 50 index (`^NSEI`)
  - SBI Life Insurance (`SBILIFE.NS`)  
  using the `quantmod` package and Yahoo Finance.

- **Return Calculation**  
  Computes daily returns from adjusted closing prices.

- **Linear Regression**  
  Fits a regression model between SBI Life and Nifty 50 returns.

- **Stationarity Testing**  
  Uses Augmented Dickey-Fuller (`adf.test`) to check if the returns series is stationary.

- **Time Series Forecasting**  
  - Autocorrelation (`acf`) and partial autocorrelation (`pacf`) analysis.
  - Fits an **ARIMA** model to forecast future returns.
  - Provides diagnostic plots (`tsdiag`).

- **Volatility Modeling**  
  Implements **GARCH** and **eGARCH** models using `rugarch` to estimate and forecast volatility.

## Requirements

Make sure you have the following installed in your R environment:

- `quantmod`
- `tseries`
- `ggplot2`
- `rugarch`
- `rmgarch`

You can install them using:

```R
install.packages(c("quantmod", "tseries", "ggplot2", "rugarch", "rmgarch"))
```

## How to Run

1. Open the notebook `FRAM Code.ipynb` in Jupyter.
2. Ensure your Jupyter environment supports R (e.g., IRkernel is installed).
3. Run the notebook cells in sequence.
4. View the analysis results, model summaries, forecasts, and diagnostic plots.

## Output

- Regression summary between SBI Life and Nifty 50.
- Stationarity test results.
- ARIMA model predictions for next 10 periods.
- GARCH-based volatility forecasts.

## Notes

- The analysis period in the notebook is set from **2020-11-02** to **2023-10-26**.  
- You can modify the date range in the `getSymbols.yahoo` calls.
