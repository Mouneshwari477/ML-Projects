# Walmart Sales Forecasting using Machine Learning

## 📌 Overview
This project predicts weekly sales for Walmart stores using historical sales data, economic indicators, and store-level features. The goal is to help the business anticipate demand, reduce stockouts, and optimize staffing/inventory decisions around seasonal and holiday trends.

## 🎯 Problem Statement
Walmart faces challenges in accurately predicting demand due to unforeseen factors like holidays, economic conditions (CPI, fuel price, unemployment), and seasonal trends. Inaccurate forecasting leads to stock shortages or overstocking. This project builds a regression model to forecast weekly sales across 45 stores using historical data.

## 🔧 Approach
1. **Data Exploration (EDA)** – Merged sales, store, and macroeconomic feature datasets; analyzed weekly/yearly sales trends, store-wise performance, and target variable distribution.
2. **Data Preprocessing** – Handled missing values (mean imputation for CPI/Unemployment, zero-fill for markdowns), encoded categorical variables (IsHoliday, Store Type).
3. **Feature Selection** – Addressed high multicollinearity using the VIF (Variance Inflation Factor) technique to shortlist relevant features.
4. **Predictive Modelling** – Benchmarked 5 regression algorithms (Linear Regression, XGBoost, CatBoost, LightGBM, Random Forest) using RMSE on a validation split; selected Random Forest for final predictions based on performance and generalizability.

## 📊 Key Insights
- **Unemployment vs. Sales:** As unemployment rises, customers buy mainly during holidays and prioritize necessary products — savings behavior increases.
- **Seasonality:** Sales peak sharply in November–December (holiday season) and drop in January.
- **Weather Effect:** Sales rise slightly with lower temperatures (outside holiday weeks).
- **Economic Correlation:** CPI and Fuel_Price are positively correlated with Weekly_Sales; Unemployment is negatively correlated.
- **Store Performance:** Top stores — 20, 4, 14, 13, 2. Weakest stores — 33, 5, 36, 38, 3. Gap between best and worst performing stores: **~$3.6M** in weekly sales.
- **Store Variability:** Store 35 shows high sales variance with no consistent pattern, spiking only during holidays.
- **Business Recommendation:** Increase casual staffing in Nov–Dec, encourage permanent staff leave in January, and prioritize marketing spend on high-demand products during holiday weeks (Christmas, Super Bowl).

## 🛠️ Tech Stack
- **Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Plotly, SciPy, Scikit-learn, XGBoost, CatBoost, LightGBM
- **Techniques:** EDA, VIF Feature Selection, Regression Modelling, RMSE Evaluation

## 📈 Results
Random Forest Regressor was selected as the final model based on comparable and generalizable RMSE performance across validation data, and used to generate final sales predictions on the test set.

# Gold Price Forecasting using Time Series Analysis (Prophet)

## 📌 Overview
This project analyzes historical gold price trends and forecasts future prices using Facebook's Prophet time series model. It uncovers weekly and seasonal patterns in gold pricing and projects price movement for the upcoming year to support trend-based decision-making.

## 🎯 Problem Statement
Gold prices fluctuate due to market cycles, seasonal demand (festivals, cultural events), and macroeconomic factors. This project builds a time series forecasting model to identify recurring patterns and predict future gold prices, helping anticipate price peaks and troughs.

## 🔧 Approach
1. **Data Cleaning** – Checked for missing values and converted the Date column to proper datetime format.
2. **Exploratory Analysis** – Visualized price distribution (identifying multi-modal clustering around distinct price bands) and analyzed monthly/yearly average price trends.
3. **Time Series Resampling** – Aggregated data at monthly and 6-month intervals to smooth short-term noise and highlight long-term trends.
4. **Forecasting with Prophet** – Trained a Prophet model on the full price history and generated a 365-day future forecast, then decomposed the forecast into weekly, yearly, and trend components.

## 📊 Key Insights
- **Price Distribution:** Gold prices cluster around distinct historical bands (~₹28k, ₹48k, ₹60k, ₹72k), with the highest trading frequency between ₹27,000–₹32,000 and ₹47,000–₹52,000, reflecting multiple market cycles over time.
- **Weekly Pattern:** Prices tend to rise on Mondays (market open) and Fridays (market close).
- **Yearly Pattern:** A price rise is observed before May — potentially linked to increased buying around Akshay Tritiya — followed by a decline, with a mild secondary peak around November.
- **Forecast:** The model projects gold prices for 2025 to range between a low of ~₹78,000 and a peak of ~₹90,000.

## 🛠️ Tech Stack
- **Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib, Prophet (time series forecasting)
- **Techniques:** Time Series Resampling, Trend & Seasonality Decomposition, Prophet Forecasting

## 📈 Results
The Prophet model successfully captured weekly and yearly seasonality in gold prices and produced a 1-year forward forecast, providing a data-driven price range for trend analysis and planning.
