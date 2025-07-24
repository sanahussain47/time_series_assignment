# time_series_assignment

Stock Price Prediction using ARIMA and LSTM
This project explores time series forecasting for stock prices using two approaches:

ARIMA — a statistical method suitable for linear, stationary time series.

LSTM (Long Short-Term Memory) — a type of deep learning model capable of learning complex, non-linear, and non-stationary patterns.

Objective
To compare the predictive performance of ARIMA and LSTM models in forecasting stock prices, and evaluate them using statistical and visual metrics.

 Data Description
Dataset: Daily stock price data (e.g., Open, High, Low, Close).

Focus Column: Close prices.

Preprocessing: Missing value handling, normalization (for LSTM), and differencing (for ARIMA).

 Model 1: ARIMA
Test for Stationarity: Augmented Dickey-Fuller (ADF)

p-value = 0.8897 → Non-stationary

Model Used: Auto ARIMA with differencing (d=1)

Evaluation:

MAE: 5.38

RMSE: 6.89

Observation: ARIMA performs poorly due to non-stationary nature of the data.

 Model 2: LSTM
Architecture: 1 LSTM layer + Dense output

Preprocessing: MinMax scaling + windowed sequences

Evaluation:

MAE: 4.07

RMSE: 5.07

Observation: LSTM captures complex trends better and follows actual price curves closely.

Key Findings
Model	MAE	RMSE	Conclusion
ARIMA	5.38	6.89	Limited by non-stationary data
LSTM	4.07	5.07	Best performance, robust learning

LSTM outperforms ARIMA in both accuracy and generalization.

