# Seoul-Bike-Rental-Prediction---ML-Supervised
# INTRODUCTION-
----------------------------
The bike sharing systems are very innovative ways of renting bicycles for use without having a burden of responsibility of ownership. This bike sharing model works in two modes -first user can get a membership for cheaper rates, second- take and pay for the bicycle on an hourly basis. The user of this system can pick up a bicycle from a Kiosk in one location and sign out to the kiosk in any designated location of the city. In recent times this bike sharing system has gained a lot of attention around the world and also feasibility studies are being taken up all over the world,places like China ,Australia ,Sao Paulo to understand the infrastructural requirements as well as the benefits and impact of the same on the citizens. With more than 500 bike renting schemes across the globe. popular bike renting programs functional in London ( Boris bikes ),Washington (capital bike share) and New York (City bikes) which are used by millions of citizens every month.this scheme provides a very wide variety of data set for analysis purpose, this promoted the team to take up the interesting problem and the challenges faced for inventory management. In a bike sharing system which can be formulated as a 'bike sharing demand' problem wherein given a supervised set of data you have to create a model to predict the number of bikes that will be rented at the given hour in the future.

# PROBLEM STATEMENT-
------------------------------------------------
Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.

# Objective-
-----------------------------------------------
The main objective of the project is to build a model to predict the demand of rental bikes and the bike count required at each hour for the stable supply of rental bikes.

# Data Description-
------------------------------------------------
The dataset contains weather information (Temperature, Humidity, Windspeed, Visibility, Dewpoint, Solar radiation, Snowfall, Rainfall), the number of bikes rented per hour and date information.

# Attribute Information:
-----------------------------------------------
➢ Date : year-month-day ➢ Rented Bike count - Count of bikes rented at each hour ➢ Hour - Hour of he day ➢ Temperature-Temperature in Celsius. (%) ➢ Humidity - a quantity representing the amount of water vapor in the atmosphere or in a gas. ➢ Wind speed - The rate at which air is moving in a particular area ➢ Visibility - a measure of the distance at which an object or light can be clearly discerned (10m) ➢ Dew point temperature - The temperature below which the water vapor in a volume of air at a constant pressure will condense into liquid water ➢ Solar radiation - The electromagnetic radiation emitted by the sun (MJ/m2) ➢ Rainfall - the quantity of rain falling within a given area in a given time (mm) ➢ Snowfall - the quantity of snow falling within a given area in a given time (cm) ➢ Seasons - Winter, Spring, Summer, Autumn ➢ Holiday - Holiday/No holiday ➢ Functional Day - NoFunc(Non Functional Hours), Fun(Functional hours

# Dataset Prepping-
---------------------------------------------
The dataset has 8,760 observations, with each observation representing one hour of one day. The target variable is ‘Rented Bike Count’ and there were 14 attributes to work with. The baseline rental count for any given day is 735 bikes.

There are no NaN values in the dataset.
## Changed the format of the Date.
Added some columns which are extracted from the Date column.

# APPROACH-
----------------------------------------------------
We performed the Outliers treatment and normalized the features for better results.Also,validate the data using VIF factor to check the multicollinearity in the dataset. One hot encoding technique is applied to create a new dataframe for model fitting.We use supervised learning regression analysis Linear Regression, Lasso Regression, Random Forest Regression,Decision Tree regressors and Gradient Boosting Regressors for the purpose of training the dataset to predict future supply and demand of bikes. Hyperparameter tuning plays an important role to predict the best model among the above regression models.

# Description
-------------------------------------
![184524446-0d6b1ccf-35d6-4f0d-921c-ef63b8ffc77f](https://user-images.githubusercontent.com/95495685/185735597-7db6b06e-d687-4fe0-bc39-637bb44e7cdc.png)



# OUTLIERS ANALYSIS-
--------------------------------------------------
![184524458-a1dcec10-0fc1-4849-b637-4eeae2a1fb5d](https://user-images.githubusercontent.com/95495685/185735622-a2306c1a-c603-4ef3-b28e-5ad308b4d13e.png)


# CORRELATION HEATMAP-
------------------------------------------
To refine the data further, a correlation matrix was created amongst all the feature variables to analyze interaction effects.

![184524469-08fa677c-37f1-4c5c-a103-709f9ead9526](https://user-images.githubusercontent.com/95495685/185735641-4df18c4e-b07a-4b1c-9267-312553c3d49c.png)

# MULTICOLLINEARITY-
-------------------------------------------------------
![184524482-c19ddfe5-809d-4845-a130-caec01187ced](https://user-images.githubusercontent.com/95495685/185735659-2ede2efd-52c1-40b6-b25c-bfb42170157d.png)

From above Dataframe, we see that there is Multicollinearity in our Data for- Dew point temperature(°C) and Humidity(%) has highest VIF value

# MODELS-
----------------------------------------------------------
## ➔ Linear Regression

![184524500-f1bf770b-7ddc-497a-b400-cdb0fd166323](https://user-images.githubusercontent.com/95495685/185735682-ecc9f889-bd6b-41f6-a44b-9b2852a1972a.png)

## ➔ Decision Tree regressors
![184524519-da3e58e9-27a3-4c7d-8f35-834724b7f45e](https://user-images.githubusercontent.com/95495685/185735696-70db23b0-4b62-4b77-84ae-f2ba05496d3a.png)


## ➔ Random Forest Regressors

![184524536-aaeb6c4e-eefc-452e-87e5-21055d689c6f](https://user-images.githubusercontent.com/95495685/185735707-d7c74453-42d7-47eb-b505-faa5a787da49.png)

## ➔ Gradient Boosting Regressors

![184524542-3371aed0-b89d-4c41-96e2-afd65263f0cb](https://user-images.githubusercontent.com/95495685/185735718-32c0d870-9ad9-4bd6-81c5-68a6260a4824.png)

● ## Hyperparameter Tuning-
![184524552-a8d4b3c8-a389-49ea-a051-a18ac8aa23d3](https://user-images.githubusercontent.com/95495685/185735730-9b7ddafc-305c-4903-9e18-8977f4335038.png)


# Conclusions-
--------------------------------------------------------------
❏ Overall, we observe that, Linear Regression model and Lasso Regression model are worst fitted models as their accuracy is less than 50% whereas, Random Forest Regressor and Gradient Boosting Regressor are the best fitted model for the train and test data set.

❏ Random Forest Regressor has the accuracy rate of train data set 98% and test data set 81%. Also, MSE is 463.08 for the train data set and 280.61 for the test data set. After, hyperparameter tuning the accuracy rate gives the similar result for the train and test data set. 

❏ Gradient Boosting Regressor has the accuracy rate of train data set 79% and test data set 77%. Also,MSE is 463.08 for the train data set and 309.65 for the test data set. With hyperparameter tuning the accuracy of the model increases and RMSE decreases which implies that the model fitted is the best model for higher accuracy rate of regression models with the predictions.

## With Hyperparameter tuning-

Accuracy of the model of train data set is 90%
Accuracy of the model of test data set is 80%
RMSE of the model of train data set is 463.08
RMSE of the model of test data set is 285.46 
● Among all the above models we conclude that Gradient Boosting Regressor(With hyperparameter tuning) is the best fitted model for Seoul Bike Rental Prediction data set.

# Thank You..!!
