# Stock-Market-Prediction-using-LSTM

This project uses a Long Short-Term Memory (LSTM) deep learning model to forecast future Google stock prices based on historical data. It demonstrates time series forecasting using deep learning techniques with a focus on financial data.

---

##  Project Objectives

- Predict future Google stock prices using past trends.
- Explore LSTM models for sequential time series data.
- Visualize actual vs predicted prices for evaluation.

---

## Methodology

1. **Dataset Access via KaggleHub**
   - Dataset: [Google Stock Data by varpit94](https://www.kaggle.com/datasets/varpit94/google-stock-data)
   - Loaded using `kagglehub` or the official `kaggle` API.

2. **Preprocessing**
   - Used only the `Close` prices.
   - Applied `MinMaxScaler` to normalize values between 0 and 1.
   - Created time windows of 60 days to predict the 61st day.

3. **Model Architecture**
   - 2 LSTM layers (50 units each).
   - Dropout layers (20%) to prevent overfitting.
   - Dense output layer with 1 neuron for prediction.
   - Loss function: Mean Squared Error.
   - Optimizer: Adam.

4. **Training & Evaluation**
   - 80% data for training, 20% for testing.
   - EarlyStopping to avoid overfitting.
   - Visualized results using `matplotlib`.

---

## 📁 Dataset

- Source: Kaggle ([varpit94/google-stock-data](https://www.kaggle.com/datasets/varpit94/google-stock-data))
- Make sure to authenticate via `kaggle.json` or use KaggleHub for automated access.
- Replace the filename accordingly if needed (e.g., `GOOG.csv` or similar).

---

## 🛠️ Installation & Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/stock-price-lstm.git
cd stock-price-lstm

# Install dependencies
pip install -r requirements.txt
# or install manually:
pip install numpy pandas matplotlib scikit-learn tensorflow kagglehub

