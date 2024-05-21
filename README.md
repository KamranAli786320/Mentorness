##Market Price Prediction

This project uses machine learning techniques to predict market prices based on historical data. The primary model used in this project is the ARIMA model for time series forecasting.
Table of Contents

    Installation
    Usage
    Project Structure
    Data Preparation
    Feature Engineering
    Modeling
    Evaluation
    Visualization
    Contributing
##Data Preparation

###The dataset is read using pandas and preprocessed by encoding categorical variables and mapping month names to numeric values. The initial preprocessing steps include:

    Encoding categorical columns (market, state, city) using LabelEncoder.
    Mapping month names to numeric values.
    Converting year and month columns to a datetime object.
    Dropping the date column.

##Feature Engineering

###The following features are created to enhance the predictive power of the model:

    Lag features for quantity, priceMin, priceMax, and priceMod.
    Rolling mean features for quantity and priceMod.

The create_features function is used to generate these features and handle missing values.
Modeling

###The primary model used is the ARIMA model, applied as follows:

    The dataset is grouped by year and averaged to create a yearly time series.
    The data is split into training and testing sets.
    The ARIMA model is fit to the training data.
    Forecasts are made on the test data.

##Evaluation

###The model's performance is evaluated using:

    Mean Squared Error (MSE)
    R-squared Score

Results are visualized to show the forecast against actual values.
