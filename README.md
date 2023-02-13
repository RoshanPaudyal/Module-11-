# Module-11-Challange-Forecastin Net Prophet

In this activity analysing Marcadolibre financeial and user data in clever ways to make company grows. This analysis consist of 5 steps which are as follow:

## Step 1 -  Analysing Hourly Google Search Traffic 

1. Read the data into data frame:
 - As we worked on Colab for this homework, we upload the   "google_hourly_search_trends.csv" file into Colab, then store in a Pandas DataFrame.

- We then read the datframe in our notebook by setting Dtetime Index.

- We slice the dataframe to just month of May 2020 to figure figure out if there are any notiecable unsual pattern in google search trend.

2. Compare the total sum of Search trend in month of may 2020 when the company released it financial results to overall median monthly traffic.
- Calculate the total sum of traffic on May 2022 by using Sum function
- Calcluate the monhtly median search traffic across all months by using group by function.
- Compare the seach traffic for the month of May 2020 to the overall monthly median value

After comparing the seach traffic for the month of May 2020 to the overall monthly median value, we came to the conclusion that the search traffic for may 2020 was higher than the median monhly traffic.

## Step 2 - Mine the Search Traffic Data for Seasonality

1. Group the hourly search data to plot (use hvPlot) the average traffic by the day of week.

2. Using hvPlot, visualize this traffic as a heatmap, referencing the index.hour as the x-axis and the index.dayofweek as the y-axis.

3. Group the hourly search data by the week of the year and hvplot the average traffic by the week of the year.

4. Visualise and analysie the plot to answer if the serch traffic tend to increase during the winter holiday period(weeks 40 through 52)?

After analysing the search traffic we can come to the conclusion that the search traffic slightly tend to increas during the winter holidays period. 

## Step 3 - Relate the Search Traffic to Stock Price Patterns

1. Read in and plot the stock price data. 

2. Concatenate the stock price data to the search data in a single DataFrame.

3. Fill the missing values with the mean.

4. Sliced the data to just the first half of 2020 (2020-01 to 2020-06 in the DataFrame), and then use hvPlot to plot the data to visualise the trend of two different variables 'search trends" and ' Close'

we could visualise that the close price has increased after the the big deep in months of march and april. However, the search trend looks pretty consistent throuhout the time period wxcept for month march. 

5. Create a new columns in the DataFrame named “Lagged Search Trends” that offsets, or shifts, the search traffic by one hour and  "Stock Volatility", which holds an exponentially weighted four-hour rolling average of the company’s stock volatility,and Hourly Stuck Return" which holds the percent change of the company's stock price on an hourly basis

6. Review the time series correlation to figure out if there is any predictable relationship between the lagged search traffic and the stock volatility or between the lagged search traffic and the stock price returns?

 Based on the correlation table there is a week negetive correlation between stock volatility and lagged search traffic(-0.205355), and slightly positive correlation between the hourly stock return and stock volatility(0.160202), but these relationship are not particularly strong. Based on these findings we cannot say there is a predictable relationship between the lagged search traffic and the stock volatility or between the lagged search traffic and the stock price returns.

 ## Step 4 - Create a Time Series Model with Prophet

 1. Set up the Google search data for a Prophet forecasting model and rename the columns "ds" and "y" as recognised by prophet.

 2. Store the prophet as an object.

 3. Fit the model

 4. Cretae a future dataframe to hold predictions and make prediction to go as far as 2000 hours.

 5. Plot the forecast 

 6. Plot the individual time series components of the model.

 ## Step 5 - Optional(Due to the time constrain I left this section empty)
