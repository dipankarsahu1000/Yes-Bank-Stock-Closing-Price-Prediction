<h1> Project Summary </h1>

Yes Bank is a well-known private bank in India which was officially founded in the year of 2004. But since 2018, it was in the news because of a fraud case involving one of its founders: Rana Kapoor. So, we are investigating how the trends in the stock prices have been affected using predictive models like regression and its regularisations. Currently, we have the dataset containing the monthly stock prices from the year of 2005 to 2020 includes closing, starting, highest and lowest stock prices of every month.


<h1> Problem Statement </h1>

The objective is to develop a predictive model that can forcast the closing price of Yes Bank's stock on a monthly basis, by analysing the historical stock price data.

<h1> Getting to Know the Data </h1>

1. Number of Rows and Columns: 185 rows and 5 columns.
2. Number of Duplicate Values: 0 duplicate values.
3. Number of Missing/Null Values: 0 duplicate values.


<h1> Understanding The Variables </h1>

- Date: The date (the month and the year, in this case) in which we are observing the stock prices.
- Open: The price at which the first trade occured at the beginning of the session (the month of the year, in this case).
- High: The maximum trading price reached by the stock during the session.
- Low: The minimum trading price reached by the stock during the session.
- Close: The final price at which the stock traded at the end of the session.


<h1> Data Wrangling </h1>

The given dataset is very small and a pretty clean one too, containing no duplicate values and no missing/null values, so there was not much data wrangling required here. Only the 'Date' column was set as the index after converting its entries from string objects to datetime objects.


<h1> Data Visualization & Experimenting with charts </h1>

1. Candlestick Chart: 
