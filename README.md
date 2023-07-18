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

The given dataset is very small and a pretty clean one too, containing no duplicate values and no missing/null values, so there was not much data wrangling required here. Only the 'Date' column was set as the index after converting its entries from string objects to datetime objects so that it will be more convenient for the data visualisations.


<h1> Data Visualization & Experimenting with charts </h1>

The following charts were used here:

1. Candlestick Chart: This financial chart was specially used here to describe the open, high, low, close values over an adjustable range of time.
2. Line Plots: To analyse the variations in each feature over the years, especially to observe the fall of the stock prices after 2018.
3. Histogram/KDE Plots: To analyse the overall distribution of the features.
4. Boxplots: For studying the outliers.
5. Scatter Plots: For studying the correlation between the independent and dependent variables specially.
6. Correlation Heatmap: To check the correlation among all the features.
7. Pair Plot: To get an overall summary of the relationships between the variables.

<h1> Feature Engineering & Data Pre-processing </h1>

- Handling Outliers: Log transfomration was used for outlier treatment.
- Data Transformation: To deal with the skewness in the features, log transformation was used.
- Data Splitting: The data was split into train and tests datasets with a split ratio of 80:20.
- Data Scaling: The data was scaled using StandardScaler.


<h1> ML Model Implementation </h1>

The following models were fitted over the training data:

1. Linear Regression.
2. Ridge Regression (with GridSearchCV).
3. Lasso Regression (with GridSearchCV).
4. Elastic Net Regression (with GridSearchCV).

After observing the evaluation metrics of all the implemented models, 'Ridge Regression with GridSearchCV' is chosen as the final prediction model.


<h1> Hypothesis Testing </h1>

The following tests were implemented:

- 'Goldfeld-Quandt Test' is used to check whether the residuals are homoscedastic or not.
- 'Ljungbox Test' is used to check for the autocorrelation among the residuals.
- 'Shapiro-Wilk Test' is used to check if the residuals are normally distributed.



<h1> Conclusion </h1>

- Upon visualising the data, it can be clearly observed that after the year of 2018 (the year the fraud involving Rana Kapoor was exposed), the stock prices of Yes Bank went down sharply.

- The dataset was very clean. It did not contain any missing values and duplicated rows and didn't require much further data wrangling.

- There were some outliers in the features. A log transformation was implemented on all the features and de-emphasized the outliers.

- A positive skewness was observed in all the features, but the log transformation took care of it.

- A highly positive correlation was observed between the independent variables ('Open', 'High' and 'Low') and the dependent variable ('Close'). This is a good sign that the dependent variables can be predicted accurately from the indepedent variables.

- The independent variables are also positively correlated to each other, which is a case of multicollinearity. As the dataset is a very small one, removal of features was not recommended. We expect the regularisation methods to take of the multicollinearity upto some extent.

- Several regression models were implemented here and all of them were found to perform quite well and their evaluation metrics were very close to each other. But, among them, Ridge Regression with GridSearchCV was chosen as the final prediction model with an RMSE of 8.3824 and an R-2 score of 0.9938.

- Among the features, the 'High' and 'Low' features were found to have positive weights which indicates positive influence on the predictions. But, the 'Open' was found to have a negative weight which means that the presence of this feature has an negative influence on the prediction.

- The assumptions of the residuals being homoscedastic, not autocollinear and having a mean of zero are satisfied.



