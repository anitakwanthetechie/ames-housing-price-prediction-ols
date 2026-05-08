# house-price-prediction-ols
The following repository contains source code and documentation of an OLS machine learning model that was developed to predict housing prices for the Ames Dataset. 

# Dataset description
The Ames Housing dataset was compiled by Dean De Cock as a modern alternative to the classic Boston Housing dataset, and covers residential property sales in Ames, Iowa from 2006 to 2010. It contains 2,930 observations and 80 features describing nearly every aspect of a home, from lot size, neighborhood, and zoning to basement finish, garage type, kitchen quality, and more. The target variable is SalePrice, making it a popular benchmark for regression tasks. Its rich mix of numerical and categorical variables, along with real-world messiness like missing data, skewed distributions, and influential outliers, makes it a go-to dataset for practicing the full data science workflow, from exploratory analysis and feature engineering to model building and evaluation.

# Approach
1. Drop columns with > 40% data missing
2. Remove outliers recommended by dataset author
3. Perform feature engineering
4. Determine variables that have the most influence on SalePrice (credit for this work goes to teammate Loris Fossier)
5. Partitioning of data into training and test sets
6. Build OLS Model with training set
7. Analyze and remove influential data points
8. Predict housing prices using test set
9. Evaluate the model

# Results and Key Insights
The training model shows strong explanatory power (Adj. R-squared ≈ 0.833) and is statistically significant. All predictors are highly significant and with minimal multicollinearity, suggesting stable coefficient estimates. The Durbin-Watson statistic (~1.96) indicates close to no autocorrelation. However, residual diagnostics (Omnibus and Jarque-Bera tests) clearly indicate non-normality, with heavy tails and slight negative skew.

Predictive performance is consistent (R-squared ≈ 0.889), suggesting no overfitting and good generalization. RMSE ($28.1K) and MAPE (11.22%) indicate reasonably good predictive accuracy for housing prices.
