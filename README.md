Time Series
1. A year-wise box plot shows the overall trend, while a month-wise box plot shows the seasonality.
2. Resampling can help us obtain insights from the data from a different perspective.
3. Rolling window usually helps us understand better the data compared to resampling.
4. Patterns in a time series usually follow these components: Base level + Trend + Seasonality + Error
  - A time series may not have trend but have seasonality and vice versa.
  - Cyclic patterns is different from seasonal patterns such that cyclic events do not happen in fixed calendar-based intervals.
5. Additive time series
  - Value = Base level + Trend + Seasonality + Error
6. Multiplicative time series
  - Value = Base level x Trend x Seasonality x Error
7. Decomposing a time series into its components can get us the trend, seasonality and the residuals. Ideally, the residuals should NOT have any patterns as they are extracted out into the trend and seasonality.
8. A stationary time series is one where the values of the series is not a function of time - mean, variance, autocorrelation are constant over time.
  - Make a series stationary by:
    - Differencing the series (subtracting the next value with the current value)
    - Take the log of the series
    - Take the nth root of the series
    - Combination of all
  - Reason to make it stationary:
    - Removes any persistent autocorrelation (correlation of the series with its previous values; the previous values are helpful in predicting the current value)
9. One can check for seasonality of a time series by plotting the series in fixed time intervals like below and checking for repeatable patterns.
  - Hourly
  - Daily
  - Weekly
  - Monthly
  - Yearly
10. Use Autocorrelation Function (ACF) plot for more detailed inspection of seasonality.
11. Should NOT replace missing values with mean of the series, especially when the series is not stationary. Methods include:
  - Backward Fill
  - Forward Fill (usually lowest MSE)
  - Linear Interpolation
  - Quadratic Interpolation
  - Mean of nearest neighbors
  - Mean of seasonal counterparts

  * If we have enough past observations, forecast the missing values
  * If you have enough future observations, backcast the missing values

12. Approximate Entropy tells whether a time series is difficult to forecast - higher, harder.
13. Smoothing the series can remove noise effect
  - Rolling window - choose window size wisely (larger window size oversmooths the series)