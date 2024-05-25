## Stock Price Prediction

## Objective
The objective of this project is to predict the stock prices of a company using its historical data.

## 1. Data Collection
The data is collected using yfinance (Yahoo Finance) library.
We want to collect historical stock prices for Microsoft (MSFT).

## 2. Data Preprocessing 
On collecting data, we have important attributes such as Open, High, Low, Close, and Volume.
However, we realize that they're not on the same scale. We perform Standardization (StandardScaler).
To further improve the performance of our model, we create **2** new features, namely **SMA_20** (Simple Moving Average for 20 days' Close value) and **EMA_20** (Exponential Moving Average for 20 days' Close value).
We also drop any rows containing *null* values.

## 3. Exploratory Data Analysis (EDA)
We plot the Date against the Price of the stock.

## 4. Prediction Model - 1 (XGBoost)
We create the train and test sets using an 80-20 split.
We train and fit the model based on certain hyperparameters. We evaluate the model's performance using Mean Squared Error (MSE) and R-squared values.
We plot actual vs predicted stock prices to visualize our results.

## 5. Hyperparameter Tuning - 1
We perform hyperparameter Tuning using Grid Search to identify the best model.

## 6. Model Plotting - 1
We plot the Actual vs. Predicted price for the same.

## 7. Prediction Model - 2 (Neural Network)
We define the neural network with the **Adam** function as the optimizer and **relu** as the activation function.

## 8. Hyperparameter Tuning - 2
To identify the best model, we perform hyperparameter tuning to find the optimal values for the hyperparameters.

## 9. Model Plotting - 2
We plot the Actual vs. Predicted price for the same.

## Conclusion
We compare the Mean Squared Error (MSE) and R-squared values for both XGBoost and Neural Network models and conclude which performs better.

<img width="320" alt="image" src="https://github.com/mrohan2203/stock-price-prediction/assets/70047636/91546114-bb3e-4bd6-925d-5162cb15b151"><br>
Fig 1: metrics for XGBoost model<br>

<img width="320" alt="image" src="https://github.com/mrohan2203/stock-price-prediction/assets/70047636/b0d63e13-f309-4751-a417-88528ff13010"><br>
Fig 2: metrics for Neural Network model<br>

On comparing the Mean Squared Error (MSE) and R-squared values for both XGBoost and Neural Network models, we see that the Neural Network has a higher R-squared value but higher MSE than XGBoost. But the difference in R-squared value is more significant here, and therefore Neural Network is the better model.



