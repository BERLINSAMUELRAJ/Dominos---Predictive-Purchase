# Dominos - Predictive Purchase Order System

![](https://github.com/BERLINSAMUELRAJ/Dominos---Predictive-Purchase/blob/main/481661596_122210809634205100_6870617675683039272_n.jpg)

## Project Overview  
This project focuses on building a **Predictive Purchase Order System** for **Dominos**. The goal is to optimize the ingredient ordering process by predicting future pizza sales and generating accurate purchase orders. By forecasting sales, Dominos can ensure optimal ingredient availability, reduce waste, and avoid stockouts — directly improving customer satisfaction and operational efficiency.  

This project also aims to optimize Domino’s ingredient ordering process by predicting future pizza sales and generating actionable purchase orders. By forecasting demand accurately, Domino’s can ensure the right inventory levels, reduce wastage, and improve operational efficiency.

---

## Skills & Takeaways  
- Data Cleaning and Preprocessing  
- Exploratory Data Analysis (EDA)  
- Time Series Forecasting  
- Predictive Modeling  
- Business Decision Making  
- Real-world Application of Data Science  

---

## Domain  
- **Food Service Industry**  
- **Data Science**  
- **Machine Learning / Forecasting**  

---

## Problem Statement

![](https://github.com/BERLINSAMUELRAJ/Dominos---Predictive-Purchase/blob/main/dominos%20pizza%20tracker.webp)

Dominos wants to optimize its **inventory management** by predicting future pizza sales and generating purchase orders for required ingredients.  
The system should:  
- Forecast sales using historical sales data.  
- Convert sales predictions into ingredient requirements.  
- Generate a **purchase order** with accurate ingredient quantities for the upcoming week (or chosen period).  

---

## Business Use Cases  
- **Inventory Management:** Maintain optimal stock levels to meet demand.  
- **Cost Reduction:** Minimize waste and avoid over-purchasing.  
- **Sales Forecasting:** Predict trends to inform business strategies and promotions.  
- **Supply Chain Optimization:** Align ordering with forecasted demand, reducing disruptions.  

---

## Approach  

### 1️⃣ Data Ingestion & Cleaning
**Input:** `merged_data` (sales + ingredients)  
**Processes:**  
- Convert `order_date` → datetime format  
- Handle missing values (`daily_quantity`, `Items_Qty_In_Grams`)  
- Filter out low-data pizzas to ensure robust forecasting  

**Tools:** Python, Pandas

---

### 2️⃣ Exploratory Data Analysis (EDA)
**Goal:** Understand sales trends & patterns  
**Processes:**  
- Aggregate sales per pizza and per day  
- Identify top-selling pizzas  
- Visualize trends (optional)  

**Tools:** Pandas, Matplotlib, Seaborn

---

### 3️⃣ Time Series Forecasting
**Goal:** Predict future pizza demand  
**Processes:**  
- Build Prophet model per pizza (`daily_quantity`)  
- Compare with SARIMA and Random Forest models  
- Handle weekly/yearly seasonality  
- Forecast daily pizza sales for the next 7 days  

**Tools:** Prophet, Statsmodels (SARIMA), Scikit-learn

---

### 4️⃣ Forecast to Ingredient Mapping
**Goal:** Translate pizza forecasts into raw material demand  
**Processes:**  
- Merge forecast with `pizza_ingredients` table  
- Calculate `ingredient_demand_grams = forecast_qty * Items_Qty_In_Grams`  
- Convert to kilograms (`ingredient_demand_kg`)  

**Tools:** Pandas

---

### 5️⃣ Purchase Order Creation
**Goal:** Generate actionable inventory plan  
**Processes:**  
- Aggregate ingredient demand per day  
- Generate a purchase order table (`ingredient`, `quantity`, `day`)  
- Export to Excel for operational use  

**Output:** Comprehensive purchase order for the next 7 days  
**Tools:** Pandas, Openpyxl

---

### 6️⃣ Model Evaluation
**Goal:** Measure accuracy of forecasts  
**Processes:**  
- Compare Actual vs Forecasted sales  
- Calculate MAPE for Prophet, SARIMA, and Random Forest  
- Plot Actual vs Forecasted with MAPE annotations  

**Tools:** Pandas, Numpy, Matplotlib

---

### 7️⃣ Key Skills Applied
- **Python & Libraries:** Pandas, Numpy, Matplotlib, Seaborn, Prophet, Scikit-learn  
- **Time Series Analysis:** Prophet, SARIMA, Forecasting  
- **Predictive Modeling:** Random Forest, Regression  
- **Inventory Management:** Ingredient calculation, purchase order generation  
- **Data Science Workflow:** Data cleaning → EDA → Modeling → Evaluation → Business action

---

### 8️⃣ Results & Insights

![](https://github.com/BERLINSAMUELRAJ/Dominos---Predictive-Purchase/blob/main/order-Domino%E2%80%99s-Pizza-with-technology-2.jpg)

**From your results:**  
- **Prophet (9.75%)** performed the best → good choice for handling seasonality + weekly patterns in pizza demand.  
- **SARIMA (10.76%)** is close, so it’s also reliable.  
- **Random Forest (11.28%)** is slightly worse here, likely because we didn’t add many external features (like promotions, holidays, weather).

| Model             | MAPE (%) | Notes                                                                                                                                 |
| ----------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| **Prophet**       | 9.75     | ✅ Best performer; handles **seasonality** and **weekly trends** well. Ideal for pizza demand with predictable patterns.               |
| **SARIMA**        | 10.76    | Good performance; can capture **trend + seasonality**, but slightly behind Prophet. Reliable for short-term forecasts.                |
| **Random Forest** | 11.28    | Slightly worse; likely due to **limited external features** (e.g., promotions, holidays, weather). Works better with richer datasets. |

---

## Technical Tags  
`Data Cleaning` · `EDA` · `Time Series Forecasting` · `Predictive Modeling` · `Inventory Management`  
`Python` · `Pandas` · `Scikit-learn` · `ARIMA` · `SARIMA` · `Prophet` · `LSTM` · `Matplotlib` · `Seaborn`  

---

## Dataset  

### 1. Sales Dataset  
- **Fields:** Date, Pizza Type, Quantity Sold, Price, Category, Ingredients  

### 2. Ingredients Dataset  
- **Fields:** Pizza Type, Ingredient, Quantity Needed  

---

## Deliverables  
- ✅ Cleaned and preprocessed datasets  
- ✅ EDA report with visualizations  
- ✅ Predictive model with code and evaluation metrics  
- ✅ Weekly purchase order (ingredients required)  
- ✅ GitHub repository with documented code  
- ✅ Final project report with methodology, findings, and business implications  

---

## Evaluation Metrics  
- **MAPE (Mean Absolute Percentage Error)** → For forecasting accuracy  
- **Operational Impact** → Reduced waste and stockouts  
- **Business Value** → Improvement in inventory & cost management  

---

## Project Guidelines  
- Follow **best coding practices** (PEP8, modular code).  
- Use **Git** for version control.  
- Document steps clearly in code and report.  
- Ensure **reproducibility** via environment/dependency management.  

---
