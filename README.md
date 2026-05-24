# 📈 Stock Price Prediction using LSTM (RNN)

##  Overview

A deep learning model that predicts Google stock prices using an LSTM-based Recurrent Neural Network trained on historical time-series data.

The model learns patterns from past stock movements to forecast future prices.

---

##  Problem Statement

Stock prices are sequential and time-dependent. This project models them using LSTM networks to learn temporal dependencies and predict future values.

---

##  Tech Stack

- Python
- Pandas, NumPy
- Matplotlib
- Scikit-learn
- TensorFlow / Keras (LSTM)

---

##  Dataset

- Google Stock Price Dataset
  - Train: `Google_Stock_Price_Train.csv`
  - Test: `Google_Stock_Price_Test.csv`

### Features Used:
Open price (primary feature for prediction)

---

##  Approach

### 1. Data Processing
- Parsed date-indexed stock data
- Cleaned numeric columns
- Applied MinMax scaling

### 2. Sequence Creation
- Built sliding windows of 60 time steps
- Each sequence predicts the next day’s stock price

### 3. Model Architecture
Stacked LSTM Network:
- 4 × LSTM layers (50 units each)
- Dropout regularization (0.2)
- Dense output layer (1 unit)

### 4. Training
- Optimizer: Adam
- Loss: MSE
- Epochs: 100
- Batch size: 32

### 5. Prediction
- Tested on unseen data
- Inverse transformed predictions to original scale

---

##  Results

- Model captures overall stock trend direction
- Predictions are smooth and follow real price movement
- Limited accuracy due to market volatility and external factors not included

---

##  Key Learnings

- Time-series modeling using LSTM
- Importance of sequence windowing (60-step memory)
- Impact of feature scaling on neural networks
- Challenges in financial forecasting

---

##  Limitations

- Uses only Open price (univariate model)
- No external features (news, sentiment, macro data)
- Cannot capture sudden market shocks

---

##  Project Structure

```bash
stock-price-prediction/
├── Google_Stock_Price_Train.csv
├── Google_Stock_Price_Test.csv
├── notebook.ipynb
└── README.md
