🚗 Used Cars Price Prediction — Regression Modeling
This project builds a robust end-to-end regression pipeline to predict used car prices using real-world data. The focus is not just on model performance, but on clean data practices, statistical rigor, and interpretable insights.

📌 Problem Statement
Predict the price of used cars based on features like:


Year (age of car)


Mileage


Brand


Fuel type


Transmission


Location (zip prefix)


Sale month (seasonality)



⚙️ Pipeline Overview
1. Data Cleaning


Removed invalid values (e.g., unrealistic prices like 999999)


Handled missing values (median imputation for numeric features)


Treated anomalies (e.g., incorrect mileage, future year values)


Grouped rare categories to reduce noise



2. Exploratory Data Analysis (EDA)


Univariate analysis → distribution, skewness, outliers


Bivariate analysis → relationship with price


Key finding:


Price strongly depends on year (age) and mileage


Brand is a high-signal categorical feature


Model name has low predictive power





3. Feature Engineering


Created meaningful features:


car_age = current_year - year


Explored mileage_per_year




Removed redundant or low-impact features


Addressed multicollinearity (important for OLS)



4. Data Preprocessing Pipeline


Numerical features:


Median imputation


Standard scaling




Categorical features:


One-hot encoding




Built using sklearn pipelines for clean, reproducible workflow



5. Modeling Approaches
🔹 OLS Regression (Statistical Approach)


Used for interpretability


Feature selection based on p-values


Helped identify statistically significant predictors


🔹 Linear Regression (ML Approach)


Built using sklearn


Evaluated on unseen data



📊 Model Performance


R² ≈ 0.73 → Good explanatory power


MAE ≈ 4,000 → Average prediction error


RMSE ≈ 4,900 → Penalizes large errors


👉 Model performs well for general pricing trends, with some sensitivity to outliers

🔍 Key Insights


🚘 Car age is the strongest predictor of price


📉 Higher mileage → lower price, but effect depends on age


🏷️ Brand significantly impacts price (premium vs economy)


⚙️ Fuel type & transmission have secondary influence


📍 Location and seasonality show minor but noticeable effects



⚠️ Challenges Faced


Outliers in price and mileage


Multicollinearity between features (e.g., year vs age)


High-cardinality categorical variables


Noise in real-world data



🚀 Room for Improvement


Try advanced models:


Random Forest


Gradient Boosting (XGBoost, LightGBM)




Better feature engineering:


Interaction terms


Log transformation of price




Handle skewness more effectively


Use cross-validation tuning for better generalization


Incorporate external data (market trends, inflation, demand)



📈 Future Scope


Deploy as a price prediction API


Build an interactive dashboard


Add explainability tools (SHAP, feature importance)



🧠 Key Takeaways


Clean data > complex models


Feature engineering drives performance


Statistical models (OLS) help explain why


ML models help improve prediction accuracy



📦 Tech Stack


Python (Pandas, NumPy)


Scikit-learn


Statsmodels


Matplotlib / Seaborn



✅ Final Note
This project demonstrates a complete regression workflow, balancing statistical understanding and machine learning practice, making it ideal for real-world data science applications.

https://www.linkedin.com/in/shorya-bisht-a20144349/

