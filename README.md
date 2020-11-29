# Forecasting daily stock prices with uni-directional and bi-directional LSTM model

### Highlights:
- Forecast the daily Google stock prices from 2017-2020 by training a LSTM and bi-directional LSTM model on major tech companies stock prices, daily volatility index and NASDAQ technology sector index from 2010-2016. 
- Obtained relatively accurate forecasting results, with a mean absolute error of 0.001 on validation set and 1.17 on test set using uni-directional LSTM.
- Tech: Pytorch, Python (Numpy, Pandas, matplotlib)
- Work completed: Additional features added to observe local and global trends (using fourier transform), window-based scaling on train dataset, custom Dataset and LSTM model built using Pytorch, training pipeline on train and validation dataset with early stopping, testing pipeline on test set.

![Alt text](/assets/forecast_results_1.png?raw=true=50x50  "Forecasting results on validation dataset")

![Alt text](/assets/forecast_results_1.png?raw=true=50x50  "Forecasting results on test dataset")


### Dataset:
- Daily closing stock prices of major tech companies (Google, Apple, Nvidia, Microsoft), daily volatility index and NASDAQ technology sector index for the past 10 years obtained from Yahoo Finance  

### Bi-Directional LSTM:
- A bi-directional LSTM model is constructed by duplicated the first recurrent layer in the network, allowing it to have 2 layers next to each other.
- The input sequence is provided as input to the first layer and the reversed copy of the input sequence is provided as input to the second layer
- This allows the bi-directional LSTM to learn from both past and future values to predict the current value. 

### References used for learning:
-https://github.com/curiousily/Deep-Learning-For-Hackers/blob/master/03.stock_prediction.ipynb
-https://machinelearningmastery.com/develop-bidirectional-lstm-sequence-classification-python-keras/
-https://towardsdatascience.com/predicting-stock-prices-using-a-keras-lstm-model-4225457f0233
-https://towardsdatascience.com/aifortrading-2edd6fac689d
