# TimeSeriesAnalysis_Forcasting

# Week 1: What is Time Series?
- Definition: A time series is an **ordered sequence** of obeservations taken sequentially in time
- Assumption: Assume the time periods are equally spaced
- **Problem Uniqueness**: The correlation introduced by the sampling of adjacent points in time can severely restrict the applicability of the many conventional statistical methods traditionally dependent on the assumption that these adjacent observations are independent and identically distributed.
**Hence different methods are needed**


# Time series patterns & components
- Systemic: Components of the time series that have **consistency or recurrence** and **can be described and modeled** (i.e., level, trend, Seasonality.)
- Non-Systemic: Components of the time series that **cannot be directly modeled or explained** by the model (i.e., Noise.)


- Level: The baseline value for the series if it were a straight line (The average value in the series).
- **Trend:** Pattern exists when there is a long-term increase or decrease in the data. It does not have to be linear
- **Seasonal:** Pattern exists when a series is influenced by seasonal factors (e.g., the quarter of the year, the month, or day of the week). Seasonality is always of a fixed and known period
- **Cyclic**: Pattern exists when data exhibit rises and falls that are not of fixed period (duration usually of at least2 years).

<img width="670" alt="Screenshot 2024-03-24 at 11 20 02 PM" src="https://github.com/ColleenJung/TimeSeriesAnalysis_Forcasting/assets/119357849/6299cdd8-6820-47cd-9783-54739eb99f05">


<img width="674" alt="Screenshot 2024-03-24 at 11 21 27 PM" src="https://github.com/ColleenJung/TimeSeriesAnalysis_Forcasting/assets/119357849/da11e9f5-e901-49b7-a3f4-da0a6b20713b">

## Seasonal vs Cyclic?
**The timing of peaks and troughs is predictable with seasonal data, but unpredictable in the long term with cyclic data.**

<img width="660" alt="Screenshot 2024-03-24 at 11 27 02 PM" src="https://github.com/ColleenJung/TimeSeriesAnalysis_Forcasting/assets/119357849/876f52f5-d532-4a19-ab59-99df8aec5669">

- Consistency: Seasonal pattern constant length; cyclic pattern variable
length
- Length: Average length of cyclic cycle longer than length of seasonal
pattern
- Magnitude: Magnitude of cyclic cycle more variable than magnitude
of seasonal pattern

# Stochastic & Deterministic processses
- Deterministic models
• The Output of the model is fully determined by the parameter values and the initial conditions
• No randomness is involved
Example: 𝑦 = 273.15𝑡 + 40.

- **Stochastic models**
• Possess some inherent **randomness**
• The same set of parameter values and initial conditions will lead to an ensemble
of different outputs
Example: 𝑦 = 273.15𝑡 + 𝑟𝑎𝑛𝑑𝑜𝑚 𝑒𝑟𝑟𝑜𝑟

<img width="191" alt="Screenshot 2024-03-24 at 11 31 32 PM" src="https://github.com/ColleenJung/TimeSeriesAnalysis_Forcasting/assets/119357849/ad2f4816-3045-4405-85d6-3c218322b813">

- **Stochastic Process**
A sequence of random variables is called a stocahastic process

# Variance, Covariance and Correlation

<img width="616" alt="Screenshot 2024-03-24 at 11 32 41 PM" src="https://github.com/ColleenJung/TimeSeriesAnalysis_Forcasting/assets/119357849/d2526e1d-bd57-4fe8-bcea-20d198ed40b5">

<img width="614" alt="Screenshot 2024-03-24 at 11 33 06 PM" src="https://github.com/ColleenJung/TimeSeriesAnalysis_Forcasting/assets/119357849/1b1d5257-e48b-482a-b396-f222ae579365">

# Autocovariance, Autocorrelation
- Covariance and correlation: Measure extent of linear relationship between two variables (𝑥 and 𝑦).
- Autocovariance and autocorrelation: measure linear relationship between lagged values of a time series 𝑦.

# White Noise (WN)
- A sequence of independent, identically distributed random variables (i.i.d. r.v.s)
{𝑒𝑡:𝑡 = ±1,±2,±3,⋯} is called a white noise process.

<img width="650" alt="Screenshot 2024-03-24 at 11 41 35 PM" src="https://github.com/ColleenJung/TimeSeriesAnalysis_Forcasting/assets/119357849/a47e133c-9ed0-4a73-9cf8-966dfa03a41b">

<img width="645" alt="Screenshot 2024-03-24 at 11 42 06 PM" src="https://github.com/ColleenJung/TimeSeriesAnalysis_Forcasting/assets/119357849/f4625b1f-c7b1-4809-80ff-acfdc8a04abd">

- In simple words:
White noise is a time series that is purely random. Think of white noise as completely uninteresting with no predictable patterns.
- Gaussian white noise:
If the variables in the series are drawn from a Gaussian distribution, the series is called Gaussian white noise.
- Testing for white noise:
We can test for white noise ACF plot or by doing a Ljung-Box test (For more: See extra slides or Session 4)

# Random Walk (RW)
Let 𝑒 , 𝑒 ⋯ , 𝑒 be a sequence of independent, identically distributed random variables (i.i.d.random variables, i.e., white noise), each with zero mean and variance 𝜎 . 𝑒

<img width="652" alt="Screenshot 2024-03-24 at 11 44 00 PM" src="https://github.com/ColleenJung/TimeSeriesAnalysis_Forcasting/assets/119357849/bf25d61e-8390-4f06-aa90-f2daaf2074fc">

<img width="655" alt="Screenshot 2024-03-24 at 11 46 41 PM" src="https://github.com/ColleenJung/TimeSeriesAnalysis_Forcasting/assets/119357849/0e0caa2d-7a5c-4010-85fa-dcca2eec1c26">

## Key Differences:

- Stationarity: White noise is stationary; a random walk is not.
- Dependence: In white noise, observations are independent; in a random walk, each value depends on the cumulative sum of previous values.
- Predictability: White noise cannot be predicted, while a random walk has a degree of predictability in the short term

# Stationary and nonstationary
**In general, a stationary time series will have no predictable patterns in the long-term**

<img width="665" alt="Screenshot 2024-03-24 at 11 48 37 PM" src="https://github.com/ColleenJung/TimeSeriesAnalysis_Forcasting/assets/119357849/f48474a8-e8c5-46af-a1ea-5636c4b235c9">

<img width="673" alt="Screenshot 2024-03-24 at 11 48 55 PM" src="https://github.com/ColleenJung/TimeSeriesAnalysis_Forcasting/assets/119357849/34aada3c-eaee-4c63-bf5b-cffa1d3a8789">

<img width="662" alt="Screenshot 2024-03-24 at 11 58 02 PM" src="https://github.com/ColleenJung/TimeSeriesAnalysis_Forcasting/assets/119357849/479c18b1-6247-45ee-ab73-95cb5811fe64">

# Forcasting Residuals
- Definition: A residual in forecasting is the difference between an observed value and its forecast based on other observations:

<img width="654" alt="Screenshot 2024-03-24 at 11 55 05 PM" src="https://github.com/ColleenJung/TimeSeriesAnalysis_Forcasting/assets/119357849/7ccf751b-ba05-4542-a990-74e87e6094bc">

<img width="667" alt="Screenshot 2024-03-24 at 11 55 51 PM" src="https://github.com/ColleenJung/TimeSeriesAnalysis_Forcasting/assets/119357849/8aff534d-8d39-4ef7-a483-1c84ad67d8cb">

# Week 2: Identifying and Removing Trend
- A time series that exhibits a trend is a **nonstationary** time series. Modeling and forecasting of such a time series is greatly simplified if we can eliminate the trend as a first step in an exploratory analysis of such time series.
- There are also several types of adjustments that are useful in time series modeling and forecasting. Two of the most widely used are** trend adjustments and seasonal adjustments.**
Sometimes these procedures are called trend and seasonal decomposition.

## Definition: Deterministic Versus Stochastic Trends

<img width="467" alt="Screenshot 2024-04-01 at 3 51 40 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/3c6b21b6-e460-4d6d-be23-ab9940b583b7">

- Stochastic Trend(Inconsistent): The upward trend is caused by a strong correlation between the series at nearby time points.
- Deterministic Trend(Consistent): Cyclical or seasonal trend. The reason for the trend is clear

# Regression Model Evaluation

<img width="771" alt="Screenshot 2024-04-01 at 3 55 40 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/b2d970e5-b5de-4055-a5ba-05ca0fa1d657">

# ACF of Residual

<img width="771" alt="Screenshot 2024-04-01 at 3 57 04 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/4dd007b2-32bb-49e0-b6e0-56d4f90c788a">

- The forecasts from a model with autocorrelated errors are still unbiased, and so are **not “wrong”,** but they will usually have larger prediction intervals than they need to.

  
<img width="755" alt="Screenshot 2024-04-01 at 3 57 36 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/0cf305df-fa5a-43a1-9c33-1d06ce43cdec">

# Detecting Autocorrelation: Durbin-Watson Test, Breusch-Godfrey Test

<img width="752" alt="Screenshot 2024-04-01 at 3 58 28 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/d2ec17d9-093c-4d9c-9b28-0a9d2a15ad02">

<img width="773" alt="Screenshot 2024-04-01 at 3 58 44 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/12898c11-a50b-41b2-9efc-72bab09b4bab">

# TimeSeries Decomposition

<img width="774" alt="Screenshot 2024-04-01 at 3 59 18 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/c4c8291b-83a1-4da2-a506-6eccca55e339">

## Additive and Multiplicative Models – Possible Scenarios
- Example I
If a store were to increase its sales in March by 1,000 each year, then we would simply add the 1,000 sales or use an additive method to account for the fluctuation.
- Example II
If a store increases its sales each March at a rate of 50% (i.e., an increase by a factor of 1.5) the seasonal component should be applied with a multiplicative method.

<img width="771" alt="Screenshot 2024-04-01 at 3 59 38 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/59728c62-ee20-4e61-8dc9-70e7caceeb3b">

<img width="772" alt="Screenshot 2024-04-01 at 4 00 25 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/d5c01648-0820-41c5-9190-b7f9be33dc75">

# TimeSeries Smoothing & Forecast
- Smoothing is useful in discovering certain traits in a time series, such as long-term trend and seasonal components.
1) Naïve method : All forecasts for the future are equal to the last observed value of the series
2) Drift method
3) Average method : All future forecasts are equal to a simple average of the observed data.
4) Seasonal naïve method

<img width="748" alt="Screenshot 2024-04-01 at 4 07 01 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/87b0005e-a17b-4942-881a-385f6f435235">

<img width="769" alt="Screenshot 2024-04-01 at 4 07 13 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/57df1910-e223-4c03-875e-1c6e8ac93981">

<img width="758" alt="Screenshot 2024-04-01 at 4 07 28 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/e3c3134c-d0f1-49be-a15c-fdc64d436e5d">

# Holt-Winters seasonal method

<img width="771" alt="Screenshot 2024-04-01 at 4 09 33 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/ae09a6a2-fbd2-4fde-b72b-0d68a43be0a3">

1) Additive Seasonal Model
–If the amplitude of the seasonal pattern is independent of the average level within the season (i.e., the seasonal variations are roughly constant through the series.)
–The seasonal component is expressed in absolute terms in the scale of the observed series.
2) Multiplicative Seasonal Model
–If the amplitude of the seasonal pattern is proportional to the average level within the season.
–The seasonal component is expressed in relative terms (percentages.)

<img width="771" alt="Screenshot 2024-04-01 at 4 10 08 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/e012ff7f-a799-4517-b5bc-60ddaf90ef68">

# FPP package: Exponential Smoothing Methods

<img width="772" alt="Screenshot 2024-04-01 at 4 11 11 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/f3b52e14-e1c5-49a1-a4c8-055969a1a966">
