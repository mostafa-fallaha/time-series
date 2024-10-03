# ARIMA Solar Energy

This project was a bit of an educational project for me to undesrtand how to build and evaluate ARIMA models.

## ARIMA

Autoregressive Integrated Moving Average (ARIMA), is one of the key and popular time-series models.

- _Autoregressive Model (AM)_: As the name indicates, it is a regression of the variable
  against itself , that is, the linear combination of past values of the variables are used to
  forecast the future value.

- _Moving average (MA)_: Instead of past values, a past forecast’s errors are used to build
  a model.

Example:
Suppose you're predicting daily sales for a store, and you have the following sales data (in units):

| Day | Actual Sales | Forecast (F) | Error (E = Actual - Forecast) |
| --- | ------------ | ------------ | ----------------------------- |
| 1   | 100          | 102          | -2                            |
| 2   | 110          | 108          | +2                            |
| 3   | 115          | 114          | +1                            |
| 4   | 120          | 119          | +1                            |

Forecast for Day 5 = μ + (θ⋅Error from Day 4)
<br>
Where:

- μ is the overall mean of the series (111.25),
- θ is a weight (let's assume θ=0.5),
- The error from Day 4 is +1.

Now, we plug in the values:
<br>
Forecast for Day 5 = 111.25 + (0.5⋅(+1)) = 111.25+0.5 = 111.75
<br><br>

> Autoregressive (AR), moving average (MA) model with integration (opposite of
> differencing) is called the ARIMA model.

<br>

## Screenshots

<!-- | Time Series Decomposition                            | Autocorrelation Test                                 |
| ---------------------------------------------------- | ---------------------------------------------------- |
| ![Landing](./readme/time_series_decomposition_1.png) | ![Landing](./readme/time_series_decomposition_2.png) | -->

| Time Series Decomposition                          |
| -------------------------------------------------- |
| ![Landing](./readme/time_series_decomposition.png) |

| Autocorrelation Test              |
| --------------------------------- |
| ![Landing](./readme/acf_pacf.png) |

| ARIMA (1,0,1)                      | ARIMA (2,0,2)                      | ARIMA (2,1,2)                      |
| ---------------------------------- | ---------------------------------- | ---------------------------------- |
| ![Landing](./readme/arima_101.png) | ![Landing](./readme/arima_202.png) | ![Landing](./readme/arima_212.png) |

| Final ARIMA                          |
| ------------------------------------ |
| ![Landing](./readme/final_arima.png) |
