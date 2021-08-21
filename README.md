# **LSTM-Stock-Predictor**
![deep-learning.jpg](deep-learning.jpg)


---
### **Background**
Due to the high volatility of cryptocurrency, investor often want to incorporate sentiment from social media and news articles to help them in their trading strategies. One such indicator is the [Crypto Fear and Greed Index (FNG)](https://alternative.me/crypto/fear-and-greed-index/) which attempts to use a variety of data sources to produce a daily FNG value for cryptocurrency

---
### **Objective**
To use deep learning recurrent neural networks to model bitcoin closing prices. 
* Model 1 will use the FNG indicators to predict the closing price  
* Model 2 will use a window of closing prices to predict the nth closing price.

---
### **Steps**
1. **Fear and Greed Model**
   * Data Prepartion - 
     * Load the CSV files -[Bitcoin Sentiment](btc_sentiment.csv) and [Bitcoin Historical Closing Prices](btc_historic.csv) and use 10 day window of previous previous fng values
     * Use 70% of the data for training and the remaineder for testing
     * Use the MinMaxScaler to scale data between 0 and 1 for training snd testing data sets
   * Build and Train the LSTM RNN model
     * Build LSTM RNN model using Sequential from tensorflow.keras.models
     * Add input, hidden and output layers
     * Train the model
   * Evaluate the model performance

2. **Closing Prices Model**
   * Data Prepartion - 
     * Load the CSV files -[btc_sentiment]() and [](btc_historic) and use 10 day window of previous closing prices
     * Use 70% of the data for training and the remaineder for testing
     * Use the MinMaxScaler to scale data between 0 and 1 for training snd testing data sets
   * Build and Train the LSTM RNN model
     * Build LSTM RNN model using Sequential from tensorflow.keras.models
     * Add input, hidden and output layers
     * Train the model
   * Evaluate the model performance

### **Technologies/Tools/Libraries**
1. Python
2. Pandas
3. Numpy
4. tensorflow.Keras
5. sklearn.preprocessing
6. matplotlib
7. hvplot.pandas
8. Jupyter Notebook
9. tensorflow.random

----
### **Data**
* [Bitcoin Sentiment](btc_sentiment.csv)
* [Bitcoin Historical Closing Prices](btc_historic.csv)

---
### **Code**
* [Fear and Greed Model](lstm_stock_predictor_fng.ipynb)
* [Closing Prices Model](lstm_stock_predictor_closing.ipynb)

---
### **Output**

> **Which model has a lower loss?** </br>
>  Closing prices model has mean square error of 0.008, which is much less than Fear and Greed (FNG) Model has a mean square error of 0.0731. Further the loss FNG model is 0.059 where as closing price model is 0.01
>
> **Which model tracks the actual values better over time?** </br>
> Closing prices model better track values over time.
>
> **Which window size works best for the model?** </br>
> 10






