# Stock Price Prediction Model Using Machine Learning

This repository contains code and resources for a stock price prediction model using machine learning techniques.

## Overview

The project aims to predict future stock prices based on historical data using a Long Short-Term Memory (LSTM) neural network model. LSTM is a type of recurrent neural network (RNN) that is well-suited for sequence prediction tasks, making it suitable for time series forecasting like stock prices.

## Data

The historical stock price data used in this project is obtained from Yahoo Finance using the `yfinance` library. The data includes the following features:

- Date
- Open
- High
- Low
- Close
- Adj Close
- Volume

## Model Architecture

The LSTM model architecture consists of multiple layers of LSTM cells followed by dropout layers to prevent overfitting. The model is trained using the Adam optimizer and Mean Squared Error (MSE) loss function.

### Model Summary:

```plaintext
Layer (type)                Output Shape              Param #   
=================================================================
lstm (LSTM)                 (None, 100, 50)           10400     
dropout (Dropout)           (None, 100, 50)           0         
lstm_1 (LSTM)               (None, 100, 60)           26640     
dropout_1 (Dropout)         (None, 100, 60)           0         
lstm_2 (LSTM)               (None, 100, 80)           45120     
dropout_2 (Dropout)         (None, 100, 80)           0         
lstm_3 (LSTM)               (None, 80)                51520     
dropout_3 (Dropout)         (None, 80)                0         
dense (Dense)               (None, 1)                 81        
=================================================================
Total params: 133761
Trainable params: 133761
Non-trainable params: 0
```

## Usage

1. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/stock-price-prediction.git
   ```

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the `app.py` file:

   ```bash
   streamlit run app.py
   ```

4. Enter the stock symbol you want to predict and view the predictions.

## Results

The model predictions are visualized alongside the original stock prices using Matplotlib.

## Contributing

Contributions are welcome! For major changes, please open an issue first to discuss what you would like to change.

Members of this project:
Angeel Sharma,
Aditya Shubham Jha,
Adarsh Vishesh
