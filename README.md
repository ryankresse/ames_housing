## Ames Housing Regression
The goal in this [Kaggle competition](https://www.kaggle.com/c/house-prices-advanced-regression-techniques) 
is to predict the price that a house sells for given characteristics like its square footage, age and number of rooms. The dataset includes around 3000 houses that were sold in Ames, Iowa between 2006 and 2010.

#### Exploring the data
My first step was to explore the data, which you can see in EDA.ipynb. Some of my key findings were:
- SalePrice, the dependent variable, should be log transformed before fitting a regression model
- Features related to house quality, square footage, neighborhood and garages tended to have the strongest associations with SalePrice.



### Files:
- EDA.ipynb: exploring the data
- lasso.ipynb: preparing the data and fiting a lasso model
- error_analysis.ipynb: examining the errors from the lasso model
- huber.ipynb, knn.ipynb, random_forest.ipynb, ridge.ipynb, xgb1.ipynb: finding the best hyperparameters to use in a stacking ensemble
- stack_to_svr_0.1173.ipynb: creating and fitting a stacking ensemble


