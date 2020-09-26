# Forecasting daily stock prices with Bi-directional LSTM model

### Highlights:
- Forecast the daily stock prices from 2017-2020 by training a bi-directional LSTM model on daily stock prices from 2010-2017.
- Obtained accurate forecasting results, with a mean absolute error of 0.03.
- Tech: Tensorflow (Keras), Python (Numpy, Pandas, matplotlib)
- Work completed: Model architecture and hyperparameter tuning, saving best model using (EarlyStopping, ModelCheckpoint), evaluation of mean absolute forecast error 

![Alt text](/assets/forecast_results.png?raw=true "Forecasting results on test dataset")

### Dataset:
- Daily prices of Google stocks for the past 10 years were obtained from Yahoo Finance  

### Bi-Directional LSTM:
- A bi-directional LSTM model is constructed by duplicated the first recurrent layer in the network, allowing it to have 2 layers next to each other.
- The input sequence is provided as input to the first layer and the reversed copy of the input sequence is provided as input to the second layer
- This allows the bi-directional LSTM to learn from both past and future values to predict the current value. 

### References:
- This project was inspired by the following resources:

-https://github.com/curiousily/Deep-Learning-For-Hackers/blob/master/03.stock_prediction.ipynb

-https://machinelearningmastery.com/develop-bidirectional-lstm-sequence-classification-python-keras/

-https://towardsdatascience.com/predicting-stock-prices-using-a-keras-lstm-model-4225457f0233
