# SARIMA Forecasting of Monthly Air Passengers

> Course: Forecasting Methods · Semester 3

## Overview

Seasonal ARIMA modeling of the classic monthly AirPassengers series (1949-1960), with a guided notebook and an independent application notebook. Both include model identification, diagnostics and holdout comparison against simple benchmarks.

## Repository structure

- `notebooks/sarima-guided.ipynb` - step-by-step modeling with log transform, differencing and ACF/PACF.
- `notebooks/sarima-application.ipynb` - autonomous SARIMA application with `m=12` and a 12-month horizon.
- `data/air-passengers-1949-1960.csv` - the monthly passenger series used by both notebooks.

## Method

- Log transformation and seasonal/regular differencing to stabilize variance and trend.
- ACF/PACF inspection to propose candidate SARIMA orders.
- `statsmodels.tsa.statespace.sarimax.SARIMAX` fitting.
- Residual diagnostics including Ljung-Box, plus Holt-Winters and seasonal-naive benchmarks.
- sMAPE, MAE and RMSE on a holdout period.

## Results

The notebooks compare candidate SARIMA specifications against the benchmarks and select a seasonal model that captures the monthly pattern without leaving significant autocorrelation in the residuals. Exact figures and the final decision are recorded in the executed cells.

## Requirements

`statsmodels`, `pandas`, `numpy`, `matplotlib`, `scipy` and `jupyter`.

## How to run

```bash
pip install -r requirements.txt
jupyter notebook notebooks/
```

---
Author: Karla Maria Monroy Alvarez
