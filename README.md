# EXP-2--Implementation-of-time-series-analysis-and-decomposition
## AIM:
###  Illustrates how to perform time series analysis and decomposition on the monthly average temperature of a city/country and for airline passengers.

## ALGORITHM:
### STEP 1: Import the required packages like pandas and numpy
### STEP 2: Read the data using the pandas
### STEP 3: Perform the decomposition process for the required data.
### STEP 4: Plot the data according to need, either seasonal_decomposition or trend plot.
### STEP 5: Display the overall results.

## PROGRAM:

import pandas as pd
import numpy as np
from statsmodels.tsa.seasonal import seasonal_decompose
df=pd.read_csv('AirPassengers.csv')
df.head()
df.set_index('Month',inplace=True)
df.index=pd.to_datetime(df.index)
df.dropna(inplace=True)
df.plot()
result=seasonal_decompose(df['#Passengers'], model='multiplicable',period=12)
result.seasonal.plot()
result.trend.plot()
result.plot()

## OUTPUT:
### FIRST FIVE ROWS:
![image](https://github.com/gpavithra673/EXP-2--Implementation-of-time-series-analysis-and-decomposition/assets/93427264/ea7ed5df-8993-4fb5-a1ad-7a8c2eee23ec)

### PLOTTING THE DATA:
![image](https://github.com/gpavithra673/EXP-2--Implementation-of-time-series-analysis-and-decomposition/assets/93427264/ce8c83fa-c814-4e7a-a0ed-46e1b3370b0a)

### SEASONAL PLOT REPRESENTATION :
![image](https://github.com/gpavithra673/EXP-2--Implementation-of-time-series-analysis-and-decomposition/assets/93427264/93f3d306-83cd-4551-a3da-28b4cca99548)

### TREND PLOT REPRESENTATION :
![image](https://github.com/gpavithra673/EXP-2--Implementation-of-time-series-analysis-and-decomposition/assets/93427264/e0a4d61d-82f3-4913-9a60-88bd88c27c69)

### OVERAL REPRESENTATION:
![image](https://github.com/gpavithra673/EXP-2--Implementation-of-time-series-analysis-and-decomposition/assets/93427264/432c3343-81b4-4e61-b876-6739bede4dc3)
![image](https://github.com/gpavithra673/EXP-2--Implementation-of-time-series-analysis-and-decomposition/assets/93427264/78a4b385-b5d1-4be9-bebb-7b91b64d8191)

## RESULT:
### Thus we have created the python code for the time series analysis and decomposition.
