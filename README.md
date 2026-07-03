# ⚡ Electricity Demand Forecasting using Statistical & Deep Learning Models

A comparative study of **24-hour ahead electricity demand forecasting** in Brazil using traditional statistical models and deep learning techniques. This project evaluates the forecasting performance of **SARIMA, SARIMAX, RNN, and LSTM** models on hourly electricity demand data spanning **2000–2023**.

---

## 📌 Project Overview

Short-term electricity demand forecasting plays a crucial role in power system planning, energy trading, and grid reliability.

This project develops and compares both classical time-series models and deep learning architectures for **24-hour ahead electricity demand forecasting**. It also investigates the influence of meteorological variables and analyzes the effect of removing the **2001–2002 Brazilian electricity crisis** (structural break) on forecasting performance.

---

## 📊 Dataset

- **Country:** Brazil
- **Period:** 2000–2023
- **Frequency:** Hourly
- **Observations:** 201,318

### Variables

- Electricity Demand (MW)
- Air Temperature
- Apparent Temperature
- Relative Humidity
- Wind Speed
- Timestamp

---

## 🔍 Data Processing & Exploratory Analysis

- Datetime conversion and indexing
- Missing value detection and treatment
- Structural break identification
- Correlation analysis
- Violin plots and temporal distribution analysis
- Time-series decomposition
- KPSS stationarity test
- Cyclical feature engineering (hour, day, month)
- Chronological train-test split

---

## 🤖 Models Implemented

### Statistical Models
- SARIMA
- SARIMAX (Apparent Temperature)
- SARIMAX (All Weather Variables)

### Deep Learning Models
- Recurrent Neural Network (RNN)
- Long Short-Term Memory (LSTM)

---

## 📈 Evaluation Metrics

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Percentage Error (MAPE)
- Wilcoxon Signed-Rank Test

---

## 🏆 Model Performance

| Model | MAE | RMSE | MAPE |
|------|------:|------:|------:|
| SARIMA | 5285.93 | 6231.51 | 9.11% |
| SARIMAX (Apparent Temperature) | 5266.44 | 6212.18 | 9.08% |
| SARIMAX (All Weather Variables) | 5419.08 | 6379.81 | 9.35% |
| RNN | 924.30 | 1267.77 | 1.33% |
| **LSTM** | **772.92** | **997.62** | **1.14%** |

### Key Findings

- **LSTM** achieved the highest forecasting accuracy across all evaluation metrics.
- **RNN** also demonstrated excellent performance, substantially outperforming the statistical models.
- Among the statistical approaches, **SARIMAX (Apparent Temperature)** slightly outperformed SARIMA.
- Including all available weather variables did not improve forecasting performance, suggesting that additional meteorological variables introduced little predictive value.
- Removing the 2001–2002 structural break resulted in higher forecasting errors, indicating that the interruption of the natural seasonal cycle reduced the models' ability to learn recurring seasonal patterns.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Statsmodels
- PyTorch

---


## 🚀 Future Work

- Hyperparameter optimization
- Transformer- and GRU-based forecasting models
- Feature selection and additional exogenous variables
- Multi-step forecasting
- Streamlit deployment for interactive forecasting

---

## 👤 Author

**Aritra Chakraborty**  
M.Sc. Statistics & Computing  
Banaras Hindu University

---

### ⭐ If you found this project useful, consider giving the repository a star.
