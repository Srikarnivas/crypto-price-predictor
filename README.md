# 🔮 Cryptocurrency Price Predictor

A web-based application that uses deep learning (LSTM) to predict future cryptocurrency prices (e.g., Bitcoin) based on historical data. Users can enter a ticker symbol (like `BTC-USD`) and specify how many days into the future they want to predict. The app displays graphs of historical prices, model predictions, and allows CSV downloads.

---

## 📌 Features

- 📈 Fetches historical price data from Yahoo Finance
- 🧠 Uses a trained LSTM deep learning model (`model.keras`)
- 🔍 Compares actual vs predicted values
- 🚀 Predicts future prices for up to 100 days
- 📊 Displays interactive Matplotlib charts
- ⬇️ Allows users to download predictions as CSV
- 🧪 Built with Flask, TensorFlow, Keras, and Bootstrap
- 🌀 Includes a loading spinner while generating predictions

---

## 🧠 How It Works

1. The model is trained using historical closing price data from Yahoo Finance.
2. It learns from sequences of 100 days to predict the next day's closing price.
3. The trained model (`model.keras`) is loaded by the Flask backend.
4. When a user submits the form:
   - The app fetches the latest data,
   - Normalizes it using `MinMaxScaler`,
   - Feeds it to the LSTM model,
   - Displays graphs of historical, test, and future predictions.

---

## 🛠️ Installation (Run Locally)

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/crypto-price-predictor.git
cd crypto-price-predictor
```

### 2. (Optional) Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Add the Trained Model

Ensure you have a trained model file named `model.keras` in the root directory.

> You can retrain the model using the Jupyter notebook provided.

### 5. Run the Flask App

```bash
python app.py
```

Then visit:  
🌐 `http://localhost:5000`

---

## 🧪 Project Structure

```
crypto-price-predictor/
├── app.py                   # Flask backend app
├── model.keras              # Trained LSTM model (you must add this)
├── requirements.txt         # Python dependencies
├── render.yaml              # (Optional for deployment)
├── README.md                # You're reading this!
└── templates/
    ├── base.html            # Layout template
    ├── index.html           # Input form
    └── result.html          # Output results and plots
```

---

## 📓 Model Training

The LSTM model was trained on historical price data using a Jupyter notebook:

📄 `CryptoCurrency(Bitcoin) Price Prediction.ipynb`

You can re-run and retrain the model using that file. Once trained, save the model with:

```python
model.save("model.keras")
```

---

## 📦 Requirements

- Python 3.10+
- Flask
- TensorFlow 2.13+
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- yFinance

---

## ✨ Credits

- Developed by **Srikar Nivas**
- Graphs powered by Matplotlib
- UI styled with Bootstrap 5
- Price data sourced from Yahoo Finance via `yfinance`

---

## 📄 License

This project is licensed under the MIT License — feel free to use, fork, and modify it.
