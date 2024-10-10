# **Stock Price Prediction using LSTM**

This project demonstrates how to predict stock prices using historical stock data from NTT. The model employed for this task is **LSTM (Long Short-Term Memory)**, which is a type of recurrent neural network (RNN) known for capturing temporal dependencies in time-series data.

## **Project Overview**

In this project, we used NTT’s stock price data to perform the following:
- Exploratory Data Analysis (EDA) to understand the data and extract insights.
- Data preprocessing and feature engineering to prepare the data for time-series modeling.
- Model training using LSTM to predict future stock prices.
- Model evaluation using the Root Mean Squared Error (RMSE) and other relevant metrics.
- Model improvement strategies for enhancing prediction accuracy.

## **Data**
The dataset contains historical stock data for NTT, including:
- **日付け (Date)**: Date of the stock data.
- **終値 (Closing Price)**: Stock closing price for the day.
- **始値 (Opening Price)**: Stock opening price for the day.
- **高値 (High Price)**: Highest price during the day.
- **安値 (Low Price)**: Lowest price during the day.
- **出来高 (Volume)**: The number of shares traded.
- **変化率 % (Percentage Change)**: Percentage change in the stock price compared to the previous day.

### **Exploratory Data Analysis (EDA)**

We perform the following EDA steps:
1. **Descriptive Statistics**: Summary statistics of the stock data.
2. **Correlation Analysis**: Understanding the relationships between different price points.
3. **Stationarity Check**: Using the Augmented Dickey-Fuller (ADF) test to check for stationarity.
4. **Autocorrelation**: Checking if past values influence future values to identify time-series properties.

### **Modeling**

#### **Preprocessing**:
- Data was scaled between 0 and 1 using MinMaxScaler.
- Differencing was applied to the closing prices to ensure stationarity.

#### **Model Used**:
- **LSTM (Long Short-Term Memory)** model was chosen due to its capability to handle time-series data effectively.
- The model was trained using the **Mean Squared Error (MSE)** as the loss function and evaluated using **RMSE**.

### **Model Evaluation**:
- The model achieved an RMSE of **6.96**, indicating a reasonably accurate prediction for stock prices.
- The loss curve shows training and validation loss progression over epochs.

### **Model Improvement**:
- Suggestions for improvement include tuning hyperparameters (e.g., increasing LSTM units, adjusting batch size, adding more layers), increasing training epochs, and adding more features (e.g., moving averages, technical indicators).

## **Installation**

To run this notebook, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/stock-price-prediction-lstm.git
