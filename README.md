# Time-Series-Analysis
Time Series Analysis of **S&P500** Index between **Year** *2012* and *2022*

## Objective
	The project performs a preliminary analysis of the underlying time series,
	estimates forecasting models, and chooses the best one based on empirical 
	evaluations. Finally, it forecasts for 6 consecutive periods in the future 
	using the best model generated.


## Dataset
	The dataset contains daily closing values for the S&P500 index	
	between the period, Dec 2012 to Dec 2022. Below is the snapshot of the 
	same.
	
![snapshot](/data/assets/dataset.png)
	
## Data Pre-processing
	Since, the dataset contains daily records with different number of days for each month its difficult 
	to create an uniform TimeSeries. To address this problem, the average index value was calculated 
	for each month prior to instantiating the time series object. The snapshot for the updated dataset is provided below.

![pre_processed](/data/assets/preprocessed_dataset.png)

## Time-Series Plot
	With the new dataset a TS object was instantiated. Fig 3. displays the corressponding 
	time-series plot being investigated.
	
![ts_plot](/data/assets/ts_plot.png)\
          **Fig. 3**