# 🧠 Ads Click-Through Rate (CTR) Analysis and Forecasting

## 📘 Project Overview
This project analyzes and forecasts the **Click-Through Rate (CTR)** of an online advertising campaign.  
CTR measures how effectively ads engage users — calculated as the ratio of **clicks** to **impressions**.

By exploring trends, visualizing patterns, and forecasting future CTR values, this project provides insights into ad performance and user engagement behavior.

---

## 📊 Dataset Description

| Column | Description |
|--------|--------------|
| **Date** | The date on which the data was recorded |
| **Clicks** | Number of times users clicked the ads |
| **Impressions** | Number of times ads were displayed to users |

**CTR formula:**
\[
CTR = \frac{Clicks}{Impressions} \times 100
\]

---

## 🔍 Analysis Steps

### 1️⃣ Distribution of Clicks and Impressions Over Time
**Objective:** Analyze engagement and exposure trends.  
**Visualization:** Line plots showing daily clicks and impressions.

**Insights:**
- Impressions and clicks show **parallel upward trends**, indicating proportional growth.
- Seasonal fluctuations highlight varying ad visibility.

📈 *Example Plot:*  
![Clicks & Impressions Over Time](images/clicks_impressions_trend.png)

---

### 2️⃣ CTR Calculation and Visualization
**Objective:** Track how CTR evolves over time.  
**Visualization:** CTR line plot showing daily or weekly averages.

**Insights:**
- CTR increases when impressions stabilize.
- Sharp dips may reflect ad fatigue or audience targeting changes.

📊 *Example Plot:*  
![CTR Over Time](images/ctr_trend.png)

---

### 3️⃣ CTR Patterns by Day of the Week
**Objective:** Identify engagement variations by weekday/weekend.  
**Method:** Extract weekday names from `Date` and calculate mean CTR.

**Findings:**
- CTR is typically **higher during weekends**, indicating stronger engagement during leisure periods.

📅 *Example Plot:*  
![CTR by Day of Week](images/ctr_weekday_comparison.png)

---

### 4️⃣ Feature Engineering
**Created features:**
- `Day_of_Week`
- `Is_Weekend`
- `CTR` (Clicks ÷ Impressions)
- Rolling averages for smoother visualization

These features improve pattern recognition and time-series modeling.

---

### 5️⃣ CTR Forecasting (SARIMA Model)
**Objective:** Predict future CTR values using time-series forecasting.  
**Model Used:** `SARIMA(1,1,1)(1,1,1,12)`

**Steps:**
1. Checked stationarity using ADF test  
2. Differenced data to remove trend  
3. Selected hyperparameters using ACF/PACF  
4. Trained model and visualized forecast  

**Results:**
- Model effectively captures seasonal patterns in CTR.
- Forecast shows gradual improvement trend.

📉 *Example Plot:*  
![CTR Forecast](images/ctr_forecast.png)

---

## 🧰 Tools & Libraries Used

| Library | Purpose |
|----------|----------|
| **pandas** | Data manipulation & cleaning |
| **numpy** | Numerical operations |
| **matplotlib / seaborn** | Visualization |
| **statsmodels** | SARIMA forecasting |
| **datetime** | Time-based feature extraction |

---

## 📈 Key Visualizations
1. Clicks & Impressions Over Time  
2. CTR Trend Over Time  
3. CTR by Day of Week  
4. ACF & PACF for SARIMA  
5. Forecasted CTR vs Actual  

---

## 🧩 Insights Summary
- **Strong positive correlation** between impressions and clicks.  
- **Higher CTR during weekends** indicates optimal engagement times.  
- **SARIMA model** effectively captures CTR seasonality and provides accurate forecasts.  

