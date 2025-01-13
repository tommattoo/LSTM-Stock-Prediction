# LSTM-Stock-Prediction
# NVIDIA Stock Price Prediction using LSTM 💸

## Project Overview 💡
After NVIDIA's incredible bull run, I wanted to explore how accurately a deep learning model could predict its stock price movements. Using a Long Short-Term Memory (LSTM) neural network, this project aims to forecast NVIDIA stock prices based on historical data. While the predictions weren't perfect, they came impressively close, showcasing the potential of LSTM models for financial market analysis.

---

## Dataset 📊
The historical stock price data for NVIDIA was sourced using the `yfinance` Python library. The dataset includes:
- **Open price**
- **Close price**
- **High price**
- **Low price**
- **Volume**

### Data Preprocessing
- Removed unnecessary columns like `Adj Close`.
- Scaled data using MinMaxScaler to normalize values between 0 and 1.
- Split data into training (75%) and testing (25%) sets.
- Created sequences of 100 days of past data to predict the next day's closing price.

---

## Model Training 🧑🏻‍💻
The LSTM model was built and trained using TensorFlow/Keras. Key features of the model include:
1. **Four LSTM Layers**:
   - Units: 50, 60, 80, and 120 respectively.
   - Activation: ReLU.
2. **Dropout Layers**:
   - Dropout rates: 0.2, 0.3, 0.4, and 0.5 respectively to prevent overfitting.
3. **Output Layer**:
   - Dense layer with a single neuron to predict stock price.

The model was trained for 100 epochs with the Adam optimizer and Mean Squared Error (MSE) as the loss function.

---

## Evaluation and Results 📈
The model's predictions were compared against the actual test data, and the following steps were taken:
- **Visualization**: Plotted both predicted and actual prices to evaluate performance.
- **Metrics**: Computed Mean Absolute Error (MAE) to assess accuracy.
- **Tomorrow's Price Prediction**: Predicted whether the stock price would rise or fall based on the last known data point.

### Example Results
- **Actual vs. Predicted**:
  ![Stock Price Comparison](link-to-image-if-available)
- **Tomorrow's Price Prediction**:
  The model predicted whether the next day’s price would be higher or lower, with a small margin of error observed.

---

## Usage 💪🏻
To replicate this project locally:

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/nvidia-stock-lstm.git
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook:
   - Open the Jupyter Notebook.
   - Replace the ticker symbol if you'd like to predict for a different stock.

---

## Contributing 🤝
Contributions are welcome! If you have suggestions, enhancements, or bug fixes, feel free to open a pull request. Let’s improve this project together!

---

## License 🔐
This project is licensed under the MIT License.

---

## Acknowledgments 🙌
- Special thanks to the TensorFlow and Keras communities.
- Inspired by NVIDIA's groundbreaking advancements in AI and technology.

