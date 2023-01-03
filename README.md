# Time-Series-Analysis
Time Series Analysis of **S&P500** Index between **Year** *2012* and *2022*

## Objective
	The project performs a preliminary analysis of the underlying time series,
	estimates forecasting models, and chooses the best one based on empirical 
	evaluations. Finally, it forecasts for 6 consecutive periods in the 
	future using the best model generated.


## Dataset
	The dataset contains daily closing values for the S&P500 index	
	between the period, Dec 2012 to Dec 2022. Below is the snapshot of the 
	same.
	
![snapshot](./data/assets/dataset.png)\
***Fig. 1** - Snapshot of the Dataset*
	
## Data Pre-processing
	Since, the dataset contains daily records with different number of days 
	for each month, it becomes difficult to create an uniform TimeSeries. 
	To address this problem, the average index value was calculated for 
	each month prior to instantiating the time series object. The snapshot 
	for the updated dataset is provided below.

![pre_processed](./data/assets/preprocessed_dataset.png)\
***Fig. 2** - Pre-processed Dataset*

## Time-Series Plot
	With the new dataset a TS object was instantiated.  This object is a 
	vector that represents a sample of periodic data that has been 
	uniformly spaced and sorted according to time. Fig 3. displays the 
	time-series plot being investigated and which has been generated from
	the TS object.
	
![ts_plot](./data/assets/ts_plot.png)\
***Fig. 3** - Monthly Acerage Time-Series Plot for S&P500*

## Analysis

### Understanding the Time-Series Components
	Plotting the time-series together with its seasonal plots is a crucial 
	first step in understanding and subsequently forecasting a time series. 
	The charts generated are shown in the Fig 4, 5 & 6. These charts provide 
	a better understanding of the time series' components.
	
![monthly_plot](./data/assets/month_plot.png)\
***Fig. 4** - Monthly Plot of S&P500 Time-Series*


![seasonal_plot](./data/assets/seasonal_plot.png)\
***Fig. 5** - Seasonal Plot of S$P500 Time-Series*

	Following observations were made from the initial plots of the time 
	series displayed above:
	
 + There is a clear trend in the time-series
 + The seasonal plots does not indicate any presence of seasonality.
 + The time-series do not exhibit cyclical pattern.
	
	The foregoing observations are confirmed by decomposing the time series by classical method into its 
	constituent components. The decomposed plot is given 
	below. Because the series shows no seasonal variation as time 
	progresses, the seasonal component can be classified as 
	additive, and the decomposition was performed 
	accordingly using the ***additive*** model.
	
![decadd](./data/assets/decadd.png)\
***Fig. 6** - Additive Decomposition of S$P500 Time-Series*

	Consistent with the other plots, the auto-correlation figure below 
	(Fig. 7) too does not demonstrate any seasonality in the time series, 
	but it does highlight a clear upward trend.

![acf](./data/assets/ts_acf.png)\
***Fig. 7** - Auto-Correlation Function (ACF) plot of S$P500 Time-Series*

	From the above plots, the time series can be reasonably concluded 
	to thus have only trend, and randomcomponents within it.
	

## Forecasting Models

	In time-series forecasting toolkit, there are various forecasting methods 
	available ranging from very simple to most complicated. The methods used 
	for the purpose of time-series analysis of the data in this project are 
	discussed below:

