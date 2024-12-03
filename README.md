
# Cryptocurrency Price Prediction Using LSTM

Predicting cryptocurrency closing prices using **Long Short-Term Memory (LSTM)** networks, tailored for handling sequential and volatile financial market data.

![Project Screenshot Placeholder](https://via.placeholder.com/800x400?text=Add+Your+Project+Image+Here)

## 📜 Table of Contents
1. [About the Project](#about-the-project)
2. [Features](#features)
3. [Technologies Used](#technologies-used)
4. [Data Pipeline](#data-pipeline)
5. [Results and Observations](#results-and-observations)
6. [Getting Started](#getting-started)
7. [Folder Structure](#folder-structure)
8. [License](#license)

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
  - Metrics like **Mean Absolute Error (MAE)** and **Root Mean Square Error (RMSE)**.
  - Predicted vs. actual performance insights.
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
   - Historical cryptocurrency data sourced from [Kaggle](https://www.kaggle.com/).

2. **Preprocessing**:
   - Dropping irrelevant columns (e.g., `Unnamed: 0`).
   - Scaling features (`open`, `high`, `low`, `volume`, `marketCap`) and target (`close`).
   - Splitting data chronologically into training and testing sets.

3. **Model Development**:
   - Building LSTM models with varying depths and units.
   - Exploring different optimizers (`Adam`, `RMSprop`, `SGD`).

4. **Evaluation**:
   - Metrics: MAE, RMSE.
   - Predicted vs. actual prices comparison.
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

## 🚀 Getting Started

### **Prerequisites**
- Install required libraries:
  ```bash
  pip install tensorflow pandas matplotlib seaborn scikit-learn
  ```

### **Clone the Repository**
```bash
git clone https://github.com/yourusername/crypto-price-prediction-lstm.git
cd crypto-price-prediction-lstm
```

### **Run the Code**
1. Place your dataset in the `data/` folder.
2. Run the main notebook:
   ```bash
   jupyter notebook main.ipynb
   ```
3. Review visualizations and metrics generated in the notebook.

---

## 📁 Folder Structure

```
crypto-price-prediction-lstm/
├── data/                     # Dataset folder
├── models/                   # Saved model files
├── notebooks/                # Jupyter notebooks
│   └── main.ipynb            # Main implementation notebook
├── results/                  # Generated plots and performance metrics
├── README.md                 # Project documentation
└── requirements.txt          # Required libraries
```

---

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.

---

## 🎉 Acknowledgments

- [Kaggle Datasets](https://www.kaggle.com/) for cryptocurrency data.
- TensorFlow/Keras for simplifying deep learning implementations.

---

This README is designed to make your GitHub repository appealing and informative for viewers while providing all necessary details to understand, replicate, and build upon your work.
