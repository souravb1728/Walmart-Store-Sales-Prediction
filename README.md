# Walmart-Store-Sales-Prediction

We are provided with a dataset of Walmart Store level Sales. The requirement is to predict store level sales for next 12 weeks. Here we will use time siries analysis

### Predictive Modeling

Here we are going to use predictive modeling techniques to forecast the sales for each store for the next 12 weeks.

#### Time Series Analysis

- We are going to use time series modelling to predict the future sales
- We will apply SARIMAX as it takes into account the seasonality component
- Before applying SARIMAX we have to find the order(p, d, q) and seasonal order (P, D, Q, S)

#### Finding the order(p, d, q) and seasonal order (P, D, Q, S)

We will find the order using the following methods

*1. Differencing (d)*

*2. Using ACF plot (q)*

*3. Using PACF plot (p)*

*4. Using visualization for the weekly data (S)*

From the analysis we find :

**order = (1,1,1)**

**seasonal order = (1,1,1,52)**

***Creating a function which can predict the store level sales for next 12 weeks***

1. The dataset and store id will be provided as inputs

2. First we will fetch only the store data

3. Then we will create a new dataset containing only the Sales column with date as index

4. Then we will apply sarimax and fit the store data

5. Then we forecast the store sales for next 12 weeks

6. Then we plot the historical data along with forecast data and compare through visualization



*When the function is run with store id as input a graph is generated as output containing the historical data and forecast data of the particular store*

#### Conclusions from the Analysis : 

**- Using sarimax we are able to successfully predict the next 12 weeks data for any store**

**- From the visualization it is clear that the forecast has taken into account the trends and seasonality quite well to predict the future data**
