# Stock and Cryptocurrency Price Prediction using LSTM

## Introduction

Trading is a very complex endeavour. It requires a heavy knowledge of statistics, current market trends, market news and a little bit of luck. In this notebook we will be training a machine learning model to predict the future price of a stock or a cryptocurrency based on the historical closing price data. 

To improve our chances for success we will be using an LSTM model. LSTM stands for Long Short Term Memory and is a type of recurrent neural network (RNN). RNNs are a type of neural network that can remember the previous state of the model and use it in the current state. This is very useful for time series data like stock prices.

Note that this model cannot be used to predict the price of a stock or cryptocurrency with 100% accuracy. It is just a tool to help you make better trading decisions based on historical data and should not be used as the sole basis for your trading strategy. As we all know markets are very volatile and can be affected by the things that happen in the real world and not always data.

## Modules used

In this notebook we use the following imported modules

- keras
- matplotlib
- numpy
- pandas
- scikit-learn
- tensorflow
- yfinance

## Installation

To run the code in this repository, you need to install the required dependencies. You can do this by following these steps:

1. Clone the repository to your local machine.
2. Navigate to the project directory.
3. Open a terminal or command prompt.
4. Run the following command to install the dependencies using pip:

    ```shell
    pip install -r requirements.txt
    ```

This command will install all the necessary packages listed in the `requirements.txt` file.

## Steps Followed

### 1.  Get the Data

The first step, of course, was to gather the data needed for training the model. I chose to use the popular currency Bitcoin and its historical closing price data. The source for this data was Yahoo Finance, which you can access it at htps://finance.yahoo.com/quote/BTC-USD/history?p=BTC-USD

The yfinance library made it very easy to retrieve the desired data. I simply passed in the ticker symbol for Bitcoin, as well as the desired start and end dates for the data. In this case, I requested all available Bitcoin data from the beginning of its records.

### 2. Data Visualization

Next, I shifted my focus to visualizing the closing price of Bitcoin over time. To achieve this, I employed the matplotlib library for plotting the data.

### 3. Data Preprocessing

In this step, I cleaned up the dataset, converting the index Date column to the right format, filtering out all unnecessary columns, removing incomplete data and scaling the dataset to get the best accuracy from training

### 4. Model Building

Continuing, I built the model that would be trained with the data. I used multiple layers of LSTM and Dense from keras to correctly filter the unnecessary data out of the neural network.

### 5. Model Testing

Moving forward, I tested the model using the remaining testing data that I had kept aside and checked the mean absolute error to confirm the accuracy of my model. 

To visualize its accuracy better I plotted the predicted data in a graph along with the test data to show the pattern followed by both graphs were alike. 

## Results

From the generated final graph I concluded that my model was successful in predicting future data based on the historical data given to it and could be used as a basis for making trades.

## Conclusion

As a conclusion I would like to stress that this model is not to be used as a sole trading strategy but as a tool to aid trading decisions for the user. Trading is a very volatile art that is influenced by a variety of external factors as well.

For more details, please refer to the code comments and the generated README file. Happy coding ❤️
