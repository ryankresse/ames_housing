# Ames Housing Regression
The goal of this [Kaggle competition](https://www.kaggle.com/c/house-prices-advanced-regression-techniques) 
is to predict the price that a house sells for given characteristics like its square footage, age and number of rooms. The dataset includes around 3000 houses that were sold in Ames, Iowa between 2006 and 2010.


## Exploring the data
My first step was to explore the data, which you can see in EDA.ipynb. I focused on finding the features most associated with sale price, which were those related to house quality, square footage, neighborhood and garages. This isn't surprising. Of course bigger, 'nicer' houses tend to sell for more. And you know what they say about location...

![Predictors of sale price](https://raw.githubusercontent.com/ryankresse/ames_housing/master/imgs/predictors.png)


## Building Models
I tried three linear models: ridge regression, elastic net and lasso, of which the lasso with an alpha of 0.001 performed best. It shrunk the coefficients for 80% of the features to zero. Below I've plotted the top 20 features by absolute value of their coefficients. MSZoning_C(all) is the largest, but it's a bit of an odd feature because it corresponds to properties with commercial zoning, and there are very few of them in the dataset.

![Lasso Coefficients](https://raw.githubusercontent.com/ryankresse/ames_housing/master/imgs/lasso_coef.png)


I also built a stacking model (stack_to_svr_0.1173.ipynb), which performed better than just the lasso.

#### Files:
- EDA.ipynb: exploring the data
- linear_models.ipynb: preparing the data and fiting a lasso model
- error_analysis.ipynb: examining the errors from the lasso model
- huber.ipynb, knn.ipynb, random_forest.ipynb, ridge.ipynb, xgb1.ipynb: finding the best hyperparameters to use in a stacking ensemble
- stack_to_svr_0.1173.ipynb: creating and fitting a stacking ensemble


