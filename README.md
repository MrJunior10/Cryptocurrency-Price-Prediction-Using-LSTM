
# Cryptocurrency Price Prediction Using LSTM

Predicting cryptocurrency closing prices using **Long Short-Term Memory (LSTM)** networks, tailored for handling sequential and volatile financial market data.

## 📜 Table of Contents
1. [About the Project](#about-the-project)
2. [Features](#features)
3. [Technologies Used](#technologies-used)
4. [Data Pipeline](#data-pipeline)
5. [Results and Observations](#results-and-observations)

---

## 🔍 About the Project

Cryptocurrency prices are highly volatile, making accurate predictions challenging. This project leverages the **power of LSTM networks**, designed for sequential data, to predict **closing prices** of cryptocurrencies based on historical data. The project explores the impact of:
- Varying LSTM configurations (layers, units).
- Optimizers (`Adam`, `RMSprop`, `SGD`).
- Train-test splits (`80-20`, `90-10`, `70-30`).

---

## ✨ Features

- **Data Preprocessing**:
  - Time-series formatting with 60-day look-back windows.
  - Normalization of data for improved model training.
- **Model Development**:
  - Comparison of models with different LSTM configurations.
  - Evaluation of optimizer impact on training and prediction accuracy.
- **Performance Comparison**:
  - Metrics like **Mean Absolute Error (MAE)** and **Test_loss and Train_loss**.
  - Predicted performance insights.
- **Train-Test Split Analysis**:
  - Analysis of how varying data splits affect model performance.
- **Predicted Next Close Price**:
  - Generate next close price predictions for different splits.

---

## 🛠️ Technologies Used

- **Python**: Programming language.
- **TensorFlow/Keras**: Building and training the LSTM model.
- **Pandas**: Data manipulation and preprocessing.
- **Matplotlib/Seaborn**: Visualization.
- **Scikit-learn**: Scaling and evaluation metrics.

---

## 🔗 Data Pipeline

1. **Data Acquisition**:
   - Historical cryptocurrency data sourced from Kaggle.

2. **Preprocessing**:
   - Dropping irrelevant columns (e.g., `Unnamed: 0`).
   - Scaling features (`open`, `high`, `low`, `volume`, `marketCap`) and target (`close`).
   - Splitting data chronologically into training and testing sets.

3. **Model Development**:
   - Building LSTM models with varying depths and units.
   - Exploring different optimizers (`Adam`, `RMSprop`, `SGD`).

4. **Evaluation**:
   - Metrics: MAE.
   - Predicted prices comparison.
   - Analysis of train-test splits and configurations.

---

## 📊 Results and Observations

### **Performance Summary**
- **Best Optimizer**: `Adam` achieved the lowest test loss and MAE in most configurations.
- **Layer Depth**: Increasing LSTM layers improved performance until overfitting appeared.
- **Train-Test Splits**: 
  - **80-20** split provided the best balance between training sufficiency and reliable testing.
  - **90-10** favored prediction accuracy but lacked sufficient training data.

### **Predicted Next Close Price**
- **80-20 Split**: $1051.42
- **90-10 Split**: $1717.96
- **70-30 Split**: $898.51

---

## 🎉 Acknowledgments

- **Kaggle** for cryptocurrency data.
- TensorFlow/Keras for simplifying deep learning implementations.

---

