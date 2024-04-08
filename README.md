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

# Week 3: ARIMA - non seasonal stationary time series

# Box-Cox Transformations

<img width="726" alt="Screenshot 2024-04-08 at 4 53 41 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/0a1fc9d3-3ada-4fa1-bc50-faaf1a0fa597">

- Problem: Unstabilized the variance.
- Motivation: Simpler patterns (i.e., additive) usually lead to more accurate forecasts.
- Approach: Decouple mean and variance to remove variance dependence on mean
- Often no transformation is needed (𝜆 = 1).
- Transformations sometimes make little difference to the forecasts **but have a large effect
on prediction intervals**

<img width="717" alt="Screenshot 2024-04-08 at 4 54 53 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/83cc9609-1c16-4485-9007-0d801b12f6be">

# Box-Jenkins Method
- The Box-Jenkins model assumes that the time series is stationary.
- Uses an iterative three-stage modeling approach:
1. Model Identification and Model Selection: Use the data and all related information to help select a sub-class of model that may best summarize the data.
2. Model Estimation: Use the data to train the parameters of the model (i.e., the coefficients.)
3. Model Validation: Evaluate the fitted model in the context of the available data and check for areas where the model may be improved.

# Autoregressive (AR) Process

<img width="719" alt="Screenshot 2024-04-08 at 5 06 00 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/b8600392-94d6-4a16-8359-864b35b13c66">

- Autoregressive processes are as their name suggests—**regressions on themselves.**

<img width="727" alt="Screenshot 2024-04-08 at 5 10 17 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/fdfac4c1-7f16-49d8-a273-7117429cf3dd">

Notes:
Since φ < 1, the magnitude of the autocorrelation function decreases exponentially as the
number of lags 𝑘 increases.
• If 𝟎 < 𝝓 < 𝟏, all correlations are positive.
• If −𝟏 < 𝝓 < 𝟎, the lag 1 autocorrelation 𝜌 = φ is negative, and the signs of successive 1
autocorrelations alternate with their magnitudes decreasing exponentially.

<img width="731" alt="Screenshot 2024-04-08 at 5 10 34 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/3c9c61ea-975d-403b-9312-4517b1dcf20b">

# Phi Φ(𝐵) Operator

<img width="724" alt="Screenshot 2024-04-08 at 5 12 45 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/85463a58-7279-498c-ba4a-c1d51caba6bb">

# Moving Average (MA) Process
- 𝑀𝐴(𝑞) Model Take Away: The autocorrelation function “cuts off” after lag q; that is, it is zero.
- **pure 𝑴𝑨(𝒒) process is always a stationary process**
- Note 1 : MA and Stationarity
Since the 𝑀𝐴(𝑞) is a special case of the Wold’s decomposition, the 𝑀𝐴(𝑞) process is always stationary regardless of values of the weights.
<img width="731" alt="Screenshot 2024-04-08 at 5 19 46 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/d112758b-3c38-4ed1-856c-cec2a309dc96">
- Note 2 : MA and interpretation
Another interpretation of the finite order MA processes is that at any given time, of the infinitely many past disturbances, only a finite number of those disturbances "contribute" to the current value of the time series and that the time window of the contributors "moves" in time, making the "oldest" disturbance obsolete for the next observation.

# Invertibility
- It can be shown that the 𝑀𝐴(𝑞) model is invertible; **if and only if the roots of the 𝑀𝐴 characteristic equation exceed 1 in modulus.**


# Autoregressive Moving Average Process

<img width="709" alt="Screenshot 2024-04-08 at 5 22 55 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/b6e9be99-eba1-4819-98d8-07348adea133">

# Differencing

- Recall:
1)Transformations help to stabilize the variance.
2) Motivation: Make the time series stationary.
- Definition: Differencing is a method of transforming a non-stationary time series to a stationary
one. 
- This is an important step in preparing data to be used in an ARIMA model.

<img width="734" alt="Screenshot 2024-04-08 at 5 25 16 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/faac7c5a-9c18-4ad2-a8f6-589e56bfe5cc">

# Integrated Autoregressive Moving Average Model (ARIMA) Definition AR𝐼𝑀𝐴(𝑝, 𝑑, 𝑞)

<img width="732" alt="Screenshot 2024-04-08 at 5 26 35 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/d4b5cda8-74a5-49da-b23d-6c4cc253cb85">

- AR: Autoregression. A model that uses the dependent relationship between an observation and some number of lagged observations.
- I: Integrated. The use of differencing of raw observations (i.e., subtracting an observation from an observation at the previous time step) in order to make the time series stationary.
- MA: Moving Average. A model that uses the dependency between an observation and residual errors from a moving average model applied to lagged observations.
- 𝒑: The number of lag observations included in the model, also called the lag order.
- 𝒅: The number of times that the raw observations are differenced, also called the degree of differencing.
- 𝒒: The size of the moving average window, also called the order of moving average.

# PARTIAL AUTOCORRELATION FUNCTION (PACF)

<img width="720" alt="Screenshot 2024-04-08 at 5 27 19 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/08c0fbab-7c26-4f12-9744-2ae5f607151a">

<img width="732" alt="Screenshot 2024-04-08 at 5 27 42 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/639c0f52-7447-4bfd-9ed0-5601d1801194">

<img width="726" alt="Screenshot 2024-04-08 at 5 27 55 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/e980176e-c50f-465c-8f45-696840035b69">

# Extended ACF (EACF)
- The EACF method uses the fact that if the AR part of a mixed ARMA model is known, “filtering out“ the autoregression from the observed time series results in a pure MA process that enjoys the cutoff property in its ACF. The AR coefficients may be estimated by a finite sequence of regressions.

<img width="727" alt="Screenshot 2024-04-08 at 5 28 36 PM" src="https://github.com/ColleenJung/SP24_TimeSeriesAnalysis-Forcasting-Notebook/assets/119357849/27764f41-a88e-41ee-ba54-f93db33e420c">

