# LSTM Stock Predictor

![deep-learning.jpg](Images/deep-learning.jpg)

Due to the volatility of cryptocurrency speculation, investors will often try to incorporate sentiment from social media and news articles to help guide their trading strategies. One such indicator is the [Crypto Fear and Greed Index (FNG)](https://alternative.me/crypto/fear-and-greed-index/) which attempts to use a variety of data sources to produce a daily FNG value for cryptocurrency. You have been asked to help build and evaluate deep learning models using both the FNG values and simple closing prices to determine if the FNG indicator provides a better signal for cryptocurrencies than the normal closing price data.

In this assignment, I used deep learning recurrent neural networks to model bitcoin closing prices. One model used the FNG indicators to predict the closing price while the second model used a window of closing prices to predict the nth closing price.

Completed:

1. [Prepared the data for training and testing](#prepare-the-data-for-training-and-testing)
2. [Built and trained custom LSTM RNNs](#build-and-train-custom-lstm-rnns)
3. [Evaluated the performance of each model](#evaluate-the-performance-of-each-model)

- - -

## Instructions

### Prepared the data for training and testing

Used the starter code as a guide to create a Jupyter Notebook for each RNN. The starter code contained a function to create the window of time for the data in each dataset.

For the Fear and Greed model, I used the FNG values to try and predict the closing price. A function was provided in the notebook to help with this.

For the closing price model, I used previous closing prices to try and predict the next closing price. A function was provided in the notebook to help with this.

Each model needed to use 70% of the data for training and 30% of the data for testing.

Applied a MinMaxScaler to the X and y values to scale the data for the model.

Finally, reshaped the X_train and X_test values to fit the model's requirement of samples, time steps, and features. (*example:* `X_train = X_train.reshape((X_train.shape[0], X_train.shape[1], 1))`)

### Built and trained custom LSTM RNNs

In each Jupyter Notebook, I creatde the same custom LSTM RNN architecture. In one notebook, I fit the data using the FNG values. In the second notebook, I fit the data using only closing prices.

Used the same parameters and training steps for each model so I could compare each model accurately.

### Evaluate the performance of each model

Finally, used the testing data to evaluate each model and compare the performance.

Use the above to answer the following:

> Which model had a lower loss?
>
> Which model tracked the actual values better over time?
>
> Which window size worked best for the model?

- - -

### Resources

[Keras Sequential Model Guide](https://keras.io/getting-started/sequential-model-guide/)

[Illustrated Guide to LSTMs](https://towardsdatascience.com/illustrated-guide-to-lstms-and-gru-s-a-step-by-step-explanation-44e9eb85bf21)

[Stanford's RNN Cheatsheet](https://stanford.edu/~shervine/teaching/cs-230/cheatsheet-recurrent-neural-networks)

- - -

### Hints and Considerations

Experiment with the model architecture and parameters to see which provides the best results, but be sure to use the same architecture and parameters when comparing each model.

For training, use at least 10 estimators for both models.

- - -

© 2019 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
