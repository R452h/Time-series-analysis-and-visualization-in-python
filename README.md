# ⏳ Time Series Analysis & Visualization in Python

## 📌 Overview
This project demonstrates **time series analysis and visualization** using Python. It explores how **stock price data** changes over time and applies statistical techniques like **trend detection, seasonality analysis, stationarity testing, differencing, and smoothing**. The goal is to help understand time-based data and prepare it for forecasting models.

## 🚀 Key Concepts Covered
- **Trend** – Long-term direction of data  
- **Seasonality** – Repeated patterns at regular intervals  
- **Moving Average** – Smoothing short-term fluctuations  
- **Noise** – Random irregular components  
- **Differencing** – Making data stationary  
- **Stationarity** – Mean, variance, and autocorrelation constant over time  
- **Autocorrelation** – Similarity between time series and its lagged version  
- **Resampling** – Changing data frequency (e.g., daily → monthly)  

## 📂 Dataset
We use a **stock dataset (`stock_data.csv`)** with columns like:  
- `Date` → Time index  
- `High` → Daily high stock price  
- `Volume`, `Open`, `Close`, etc.  
👉 Make sure the dataset has a **Date column** for time-based analysis.

## ⚙️ Installation & Requirements
Install dependencies:
pip install pandas numpy seaborn matplotlib statsmodels.

## 📊 Steps Implemented

1. **Data Loading**
   ```python
   df = pd.read_csv("stock_data.csv", parse_dates=True, index_col="Date")
2. **Data Cleaning**
   df.drop(columns=['Unnamed: 0'], inplace=True, errors='ignore')
3. **Visualization – High Stock Prices**
📉 Line plot of stock highs over time
4. **Resampling**
   df.resample('M').mean()
5. **Seasonality Detection**
🔄 Autocorrelation plots with plot_acf()
6. **Stationarity Test**
🧪 ADF test (adfuller) to check stationarity
7. **Differencing**
   df['high_diff'] = df['High'].diff()
8. **Moving Average**
   df['rolling_mean'] = df['High'].rolling(window=120).mean()
9. **Comparison** → Plotted original vs differenced data & reran ADF test

**📈 Outputs**

📉 Line plot of stock prices over time

📊 Resampled monthly averages

🔄 Autocorrelation plots (seasonality detection)

🧪 ADF test results for stationarity

📉 Original vs Differenced series

📏 Moving average smoothing

**🏆 Results**

The raw stock data was non-stationary

After differencing, the data became stationary (confirmed via ADF test)

Seasonal patterns detected using autocorrelation

Smoothed moving averages revealed long-term stock price trends

**📌 Applications**

📊 Stock price analysis

🌡️ Sensor/IoT time series

📉 Forecasting (ARIMA, SARIMA, LSTM, etc.)

📆 Trend & seasonality detection in business data

<img width="1920" height="1080" alt="Screenshot (2)" src="https://github.com/user-attachments/assets/79e79b3f-6661-49e5-93f7-5d2927ff32f4" />

<img width="1920" height="1080" alt="Screenshot (3)" src="https://github.com/user-attachments/assets/46e97f28-5921-455d-8057-78f8d7047526" />

<img width="1920" height="1080" alt="Screenshot (4)" src="https://github.com/user-attachments/assets/006e2981-360e-486f-9c1f-297d015b9eeb" />

<img width="1920" height="1080" alt="Screenshot (5)" src="https://github.com/user-attachments/assets/9df9454b-93d7-4ab0-85fd-8887f364a768" />

<img width="1920" height="1080" alt="Screenshot (6)" src="https://github.com/user-attachments/assets/bdcfac7b-5704-47f1-b85a-f420aa334732" />

<img width="1920" height="1080" alt="Screenshot (7)" src="https://github.com/user-attachments/assets/05a8a477-e008-4adb-9684-f754071b9f5a" />

<img width="1920" height="1080" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/c61cea6c-aafe-439b-aded-ed84054b7738" />













