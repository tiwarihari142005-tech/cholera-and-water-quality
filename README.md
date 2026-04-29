# 🦠 Global Cholera Analytics & Mortality Prediction

This project explores historical global cholera data (1949 – 2016) to identify trends, geographical hotspots, and risk factors. It utilizes Machine Learning to predict the number of deaths based on reported cases and fatality rates.

## 🚀 Project Overview
Cholera remains a global threat to public health. This notebook performs a comprehensive **End-to-End Data Science workflow**:
1.  **Data Cleaning:** Handling missing values and type conversions.
2.  **Exploratory Data Analysis (EDA):** Visualizing global trends and regional impacts.
3.  **Machine Learning:** Comparing Linear Regression and Random Forest Regressors to predict mortality.

## 📊 Key Insights
* **Most Affected Country:** India (Total Cases & Deaths).
* **Worst Year Globally:** 1991.
* **Highest Risk Region:** South-East Asia (Highest average fatality rate).
* **Primary Predictor:** Number of reported cases is the strongest feature for predicting deaths.

## 🛠️ Technical Stack
* **Language:** Python
* **Libraries:** * `Pandas` & `NumPy` for data manipulation.
    * `Matplotlib` & `Seaborn` for data visualization.
    * `Scikit-Learn` for preprocessing and machine learning.

## 🤖 Machine Learning Performance
Initially, a Linear Regression model was tested but performed poorly due to outliers and non-linear relationships. By switching to a **Random Forest Regressor** and removing outliers, the model performance improved significantly:

| Model | R² Score | RMSE |
| :--- | :--- | :--- |
| Linear Regression | -0.7880 | 2167.43 |
| **Random Forest Regressor** | **0.8786** | **46.97** |

> **Note:** The Random Forest model explains approximately **87.8%** of the variance in the death toll data, making it a highly reliable predictor for this dataset.

## 📂 Dataset Structure
The dataset contains **2,492 records** with the following features:
* `Country`: Name of the country.
* `Year`: Year of report (1949–2016).
* `Cases`: Number of reported cholera cases.
* `Deaths`: Number of reported deaths.
* `Fatality_Rate`: Case fatality rate (%).
* `WHO_Region`: Geographical region classification.

## 📈 Visualizations Included
1.  Top 10 Countries by Total Cases.
2.  Global Yearly Case Trends.
3.  Total Deaths by WHO Region.
4.  Correlation Heatmap of features.
5.  Actual vs. Predicted Mortality Scatter Plot.

---

### How to Run
1.  Clone this repository.
2.  Ensure you have the `data.csv` file in the correct directory.
3.  Install dependencies: `pip install pandas numpy matplotlib seaborn scikit-learn`.
4.  Run the Jupyter/Kaggle notebook.
