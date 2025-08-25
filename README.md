# 🪙 Gold Price Prediction using Machine Learning  

## 📌 Project Overview  
Gold has always been a critical investment instrument, and predicting its price accurately helps traders, investors, and analysts make informed decisions.  

This project implements a **Machine Learning model** to predict the price of **Gold (GLD)** using key financial indicators such as:  
- 📊 **S&P 500 Index (SPX)**  
- 🛢️ **Crude Oil Price (USO)**  
- 🥈 **Silver Price (SLV)**  
- 💱 **EUR/USD Exchange Rate**  

The model is trained on historical data and achieves **high prediction accuracy**.  

---

## ⚙️ Tech Stack & Libraries  
- **Python** 🐍  
- **Pandas** → Data manipulation  
- **Matplotlib / Seaborn** → Data visualization  
- **Scikit-learn** → Machine Learning (Random Forest Regressor)  

---

## 📂 Dataset Information  
The dataset used contains the following columns:  

| Feature   | Description |
|-----------|-------------|
| Date      | Date of record |
| SPX       | S&P 500 Index value |
| USO       | Crude Oil price |
| SLV       | Silver price |
| EUR/USD   | Currency exchange rate |
| GLD       | Gold price (target) |

✅ We removed the **Date** column (not useful for training)  
✅ Features (`SPX, USO, SLV, EUR/USD`) were used to predict **GLD**  

---

## 📊 Data Analysis & Visualization  

### 🔹 Correlation Heatmap  
We first analyzed the correlation between features and target:  
- SPX → Negative correlation  
- USO → Moderate correlation  
- SLV → Strong positive correlation  
- EUR/USD → Weak correlation  
- GLD → Target variable
<img width="641" height="638" alt="image" src="https://github.com/user-attachments/assets/23ecea32-7c37-45cf-8a8e-07964ee3c674" />

📈 Heatmap showed **Silver (SLV)** has the strongest correlation with **Gold price (GLD)**.  

---

## 🤖 Model Training  

We used **Random Forest Regressor** because:  
- Handles non-linear data well  
- Works well with financial time-series data  
- Provides high R² accuracy  

- 📌 **Training Score (R²)**: **0.99**  
- 📌 **Testing Score (R²)**: **0.98**  

✅ The model performs excellently with very low error.  

---

## 📉 Model Evaluation  

### 📍 Actual vs Predicted Gold Prices  
We plotted **Actual vs Predicted values**:  

- 🔴 **Actual Gold Prices**  
- 🟢 **Predicted Gold Prices**

<img width="1058" height="681" alt="image" src="https://github.com/user-attachments/assets/233947b2-5e41-4788-899e-2904e6237d27" />


The lines almost overlap → showing **very high accuracy** ✅  


---

## 🖥️ Predictive System (Console-based)  

Finally, we created a **console-based system** where the user can input financial indicators and get the predicted Gold price instantly.  

### 🔹 Example Run  

```text
🔮 Gold Price Prediction System 🔮
📊 Enter S&P 500 Index (SPX): 1447
🛢️ Enter Crude Oil Price (USO): 78.47
🥈 Enter Silver Price (SLV): 15.182
💱 Enter EUR/USD Exchange Rate: 1.47
```
### 🔹 Result 

✅ Predicted Gold Price (GLD) is: $ 84.88
