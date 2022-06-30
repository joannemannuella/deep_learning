# LSTM Stock Predictor

![deep-learning.jpg](Images/deep-learning.jpg)

Due to the volatility of cryptocurrency speculation, investors will often try to incorporate sentiment from social media and news articles to help guide their trading strategies. One such indicator is the [Crypto Fear and Greed Index (FNG)](https://alternative.me/crypto/fear-and-greed-index/) which attempts to use a variety of data sources to produce a daily FNG value for cryptocurrency. You have been asked to help build and evaluate deep learning models using both the FNG values and simple closing prices to determine if the FNG indicator provides a better signal for cryptocurrencies than the normal closing price data.

In this assignment, I used deep learning recurrent neural networks to model bitcoin closing prices. One model will use the FNG indicators to predict the closing price while the second model will use a window of closing prices to predict the nth closing price.

I did:

1. Prepare the data for training and testing
2. Build and train custom LSTM RNNs
3. Evaluate the performance of each model

- - -
This done by doing an analysis using jupyter lab on:

[Closing Prices Starter Notebook](Starter_Code/lstm_stock_predictor_closing.ipynb)

[FNG Starter Notebook](Starter_Code/lstm_stock_predictor_fng.ipynb)

- - -


### Prepare the data for training and testing

I used the starter code as a guide to create a Jupyter Notebook for each RNN. The starter code contains a function to create the window of time for the data in each dataset.

For the Fear and Greed model, I used the FNG values to try and predict the closing price. A function is provided in the notebook to help with this.

For the closing price model, I used previous closing prices to try and predict the next closing price. A function is provided in the notebook to help with this.

Each model will need to use 70% of the data for training and 30% of the data for testing.

Apply a MinMaxScaler to the X and y values to scale the data for the model.

Finally, I reshape the X_train and X_test values to fit the model's requirement of samples, time steps, and features. (*example:* `X_train = X_train.reshape((X_train.shape[0], X_train.shape[1], 1))`)

### Build and train custom LSTM RNNs

In each Jupyter Notebook, I create the same custom LSTM RNN architecture. In one notebook, I fit the data using the FNG values. In the second notebook, I will fit the data using only closing prices.

this used the same parameters and training steps for each model. This is necessary to compare each model accurately.

### Evaluate the performance of each model

Finally, use the testing data to evaluate each model and compare the performance.

From all the steps i did above, I can answer the following:

> Which model has a lower loss?

The closing price predicted model showed  lower loss than the FNG predicted model. 



> Which model tracks the actual values better over time?

The closing price predicted model showed better value over time 


> Which window size works best for the model?

The window size of 1 day works best for the model
- - -


- - -

© 2019 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
