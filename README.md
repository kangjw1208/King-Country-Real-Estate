# King County Real Estate Advice
## Overview
This project uses statistical analysis and multiple linear regression modeling to analyze housing data in King County, Washington. The purpose of this project is to provide an accurate model for Seattle based, Every Door Real Estate Company, that can be used to advise their clients on both sales and purchases of residential real estate in King County.
## Business Problem & Key Questions
As a real estate agency firm, their primary role is to connect potential buyers and sellers of real estate properties. It is therefore imperative that they provide an accurate information and services to their clients and ensure both parties consent on a fair property price. Every Door Real Estate Company needs a model that provides statistically significant information on features that impact housing value and predicts a fair price based on those features and will make ssure the client is content on their decision of choosing Every Door Real Estate Company. 

* Which specific features significantly influence the overall value of the house?
* How significant are the locations of the house within King County?
* Is it possible to predict the housing price based on its features?
* How can Every Door Real Estate Company utilize this model to increase their profit? 
## Data Understanding
The following dataset was given and used to build the model.
* data/kc_house_data.csv

The dataset was provided to allow for deep exploration into King County's housing data. The dataset included specs for over 21,000 homes with giving their square footage, rating of construction quality, number of bedrooms and bathrooms and most importantly their price. Data was collected from home sales in 2014-2015.

After some exploratory data analysis it was deemed the data wasn't in a state the would give out proper models instantly with some columns not being in a managable numeric value and others missing data. Also was determined many columns would not be useful in future model creation and they were not included in our working dataframe.

Heavy use of the efficient tools within scikit-learn's library allowed us to manage the data to allow for model creation down the  line. 
SimpleImputer to deal with missing values in our waterfront amd view columns.
OneHotEncoder to deal with non continous categorical columns and creating a binary column for each category that was represented in the column as a value.
We also removed outliers from the dataset based on the 95% Interquartile range.

Seeing that our target is our price column we tried to see which columns had a positive and substantial correlation to it. 




## Modeling
The modeling is divided into two parts: inferential and predictive. 
1) predictive modeling
2) inferential modeling 

### Predictive Modeling
We first created a baseline model using DummyRegressor from scikit-learn. We then created a simple regression model based on the top correlated feature with price (sqft_living). For our predictive model we log transformed price in order to help account for heteroskedasticity within the dataset. We also scaled sqft_living using scikit-learn's StandardScaler. Our simple model was then iterated over to produce subsequently better predictive models. We added in features to test their effects on the model. Our final model (M8) includes:
* sqft_living
* presence of waterfront
* presence of basement
* zip code
* quality of view
* condition of house
* number of floors

## Regression Results
## Recommendations and Conclusions
