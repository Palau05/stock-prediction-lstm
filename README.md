# 📈 Stock Price Prediction with LSTM (PyTorch)

A machine learning project that predicts stock prices using a Long Short-Term Memory (LSTM) neural network built with PyTorch.

## 🎯 What does this project do?

This model takes the last 60 trading days of a stock's closing price as input and predicts the next day's closing price. It was trained on Apple (AAPL) stock data from 2022 to 2024.

## 📊 Example Output

The model predicts the next trading day's closing price based on recent historical data:

```
Last known closing price:     $250.83
Predicted price for tomorrow: $249.12
```

## 🛠️ Tech Stack

- **Python 3**
- **PyTorch** – LSTM model
- **yfinance** – Stock data download
- **Pandas / NumPy** – Data processing
- **Scikit-learn** – Data normalization (MinMaxScaler)
- **Matplotlib** – Visualization

## 🚀 Getting Started

### 1. Install dependencies

```bash
pip install torch yfinance pandas numpy matplotlib scikit-learn
```

### 2. Open the notebook

Upload `Stock_Prediction_NN.ipynb` to [Google Colab](https://colab.research.google.com/) and run all cells.

### 3. Change the stock ticker (optional)

In the data loading cell, change `"AAPL"` to any stock you like:

```python
ticker = "TSLA"  # or "MSFT", "GOOGL", etc.
```

## 🧠 Model Architecture

```
LSTMModel(
  (lstm): LSTM(1, 64, num_layers=2, batch_first=True, dropout=0.2)
  (fc): Linear(in_features=64, out_features=1, bias=True)
)
```

- **Input:** 60 days of normalized closing prices
- **LSTM layers:** 2 layers with 64 hidden units
- **Dropout:** 0.2 (prevents overfitting)
- **Output:** Next day's predicted closing price

## 📁 Project Structure

```
stock-prediction-lstm/
│
├── notebook/
│   └── Stock_Prediction_NN.ipynb   # Main notebook
│
├── requirements.txt                 # Python dependencies
└── README.md                        # This file
```

## ⚠️ Disclaimer

This project is for **educational purposes only**. Stock price predictions are inherently uncertain and should not be used as financial advice.
