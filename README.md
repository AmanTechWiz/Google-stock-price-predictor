# Stock Price Prediction using LSTMs

This project implements a Long Short-Term Memory (LSTM) neural network to predict stock prices based on historical data. The model is trained using Google's stock price data and demonstrates the potential of deep learning in time-series forecasting.

---

## 🚀 Features
- **Data Preprocessing**: Scales the data for better model performance.
- **LSTM Architecture**: A multi-layered LSTM model with dropout layers to prevent overfitting.
- **Time-Series Forecasting**: Predicts future stock prices based on past trends.
- **Visualization**: Displays the predicted vs actual stock prices for evaluation.

---

## 🛠️ Installation

1. Clone the repository:

2. Install dependencies:
   ```
    pip install -r requirements.txt
3. Ensure you have the dataset (`Google_Stock_Price_Train.csv`) in the project directory.

---

## 📖 Usage

1. Open the Jupyter notebook:
   ```
     jupyter notebook stock-price-prediction.ipynb

2. Run all cells to preprocess data, train the LSTM model, and visualize results.

3. Modify the code to experiment with different datasets or model architectures.

---

## 🧠 Model Architecture

The LSTM model consists of:
- 4 stacked LSTM layers with 50 units each.
- Dropout layers (20%) after each LSTM layer to reduce overfitting.
- A Dense layer with 1 unit for output.

### Model Summary:
| Layer (type)      | Output Shape      | Param # |
|-------------------|-------------------|---------|
| LSTM              | (None, 60, 50)   | 10,400  |
| Dropout           | (None, 60, 50)   | 0       |
| LSTM              | (None, 60, 50)   | 20,200  |
| Dropout           | (None, 60, 50)   | 0       |
| LSTM              | (None, 60, 50)   | 20,200  |
| Dropout           | (None, 60, 50)   | 0       |
| LSTM              | (None, 50)       | 20,200  |
| Dropout           | (None, 50)       | 0       |
| Dense             | (None, 1)        | 51      |

Total Parameters: **71,051**

---

## 📊 Results

The model was trained for **100 epochs** and achieved a low mean squared error on the training set. The predicted stock prices closely follow the actual prices.
Acheived accuracy of 97%.

### Sample Visualization:
![image](https://github.com/user-attachments/assets/8d90a403-6fae-4a73-b35a-92483819f7b9)


---

## 🤝 Contributing

Contributions are welcome! Feel free to fork this repository and submit a pull request.

---

## 📄 License

This project is licensed under the MIT License. See `LICENSE` for more details.
