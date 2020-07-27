# Stock Price Prediction | Machine Learning

Our stock prediction platform helps to boost confidence in naïve investors by providing latest stock trends. The predictions are generated using machine learning techniques. This repo will focus on implementation and evaluation of different predictive algorithms. 

To compare the performance of various algorithms, we took 4 years of stock prices and compared the prediction accuracies. Code used for testing is summarized in "Test Algorithms.ipynb." Summary of results as follows:

| Algorithm  | RMSE |
| ------------- | ------------- |
| Linear Regression  | 34.58 |
| K-Nearest Neighbors  | 71.19 |
| Auto ARIMA  | 13.99 |
| Prophet  | 15.75  |
| Long Short Term Memory(LSTM)  | 2.15  |

From the algorithm comparisons, we decided that Long Short Term Memory is best suited for stock predictions and therefore investigated further. Code used for hyperparameter optimization is summarized in "LSTM_investigation.ipynb." Summary of results as follows:

| Algorithm  | RMSE |
| ------------- | ------------- |
| Standard Averaging  | 0.0647 |
| EMA Averaging  | ???TBD??? |
| LSTM  | 0.0509 |
***Note: sqrt(MSE) = RMSE

Code used for hyperparameter optimization is also summarized in "LSTM_investigation.ipynb" where a list of hyperparameters are altered to find the most optimized solution. List of hyperparameters involved:
1. batch_size 
2. decay_rate
3. dropout 
4. num of unrollings
5. epochs 
6. num of nodes

Conclusions:


| Varied Parameter  | RMSE |
| ------------- | ------------- |
| Decreased batch size  | decrease |
| Decreased dropout value  | decrease |
| Decreased number of nodes | decrease |
| Decreased number of layers(200 nodes)  | decrease |
| Decreased number of layers(1500 nodes)  | increase |
| Decreased number of unrollings  | increase  |
