# Dominos - Predictive Purchase Order System  

![](https://github.com/BERLINSAMUELRAJ/Dominos---Predictive-Purchase/blob/main/481661596_122210809634205100_6870617675683039272_n.jpg)

## Project Overview  
This project focuses on building a **Predictive Purchase Order System** for **Dominos**. The goal is to optimize the ingredient ordering process by predicting future pizza sales and generating accurate purchase orders. By forecasting sales, Dominos can ensure optimal ingredient availability, reduce waste, and avoid stockouts — directly improving customer satisfaction and operational efficiency.  

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

### 1️⃣ Data Preprocessing & Exploration  
- **Data Cleaning:** Handle missing values, inconsistencies, and outliers.  
- **Formatting:** Convert date/time formats and standardize categories.  
- **EDA:** Identify sales trends, seasonality, and key demand drivers.  
- **Visualization:** Explore sales by pizza type, day of week, month, promotions, and holidays.  

### 2️⃣ Sales Prediction  
- **Feature Engineering:** Extract time-related features (day, month, holiday, promo).  
- **Model Selection:**  
  - Traditional: ARIMA, SARIMA  
  - Advanced: Facebook Prophet, LSTM, Regression Models  
- **Training:** Train predictive models using historical sales data.  
- **Evaluation:** Evaluate models using **Mean Absolute Percentage Error (MAPE)**.  

### 3️⃣ Purchase Order Generation  
- **Forecasting:** Predict pizza sales for the upcoming week.  
- **Ingredient Mapping:** Translate sales forecasts into ingredient requirements using the ingredient dataset.  
- **Purchase Order Creation:** Generate a structured order report specifying each ingredient’s required quantity.  

---

## Results

![](https://github.com/BERLINSAMUELRAJ/Dominos---Predictive-Purchase/blob/main/order-Domino%E2%80%99s-Pizza-with-technology-2.jpg)

- **Accurate sales predictions** based on time series and regression models.  
- **Purchase Order Report** with detailed ingredient requirements.  
- Improved **inventory efficiency** — reducing waste and preventing shortages.  

---

## Observations  
- **ARIMA/SARIMA** → Works well for short-term seasonality but struggles with irregular holiday effects.  
- **Prophet** → Handles seasonality and holidays better, producing more stable forecasts.  
- **LSTM** → Captures complex non-linear patterns but requires large amounts of data and tuning.  
- **Regression Models** → Useful as a baseline, but limited in handling temporal dependencies.  

👉 Overall, **Prophet** performed best in this project due to its ability to handle multiple seasonalities and holiday effects, while **LSTM** showed potential but required more computational resources.  

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

## Repository Structure (Suggested)  
