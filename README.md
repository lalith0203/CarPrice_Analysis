# CarDekho Used Car Price Analysis & Prediction

This project focuses on analyzing used car data from CarDekho and building a regression model to predict the number of kilometers a car has been driven based on various features like price, age, fuel type, seller type, transmission, and ownership history.

---

## 📁 Dataset

- **Source:** `CAR DETAILS FROM CAR DEKHO.csv`
- **Entries:** 4340
- **Columns:** 8
- **Features:**
  - `name`: Car model
  - `year`: Manufacturing year
  - `selling_price`: Price at which the car is listed
  - `km_driven`: Kilometers the car has been driven
  - `fuel`: Fuel type (Petrol/Diesel/LPG/CNG)
  - `seller_type`: Type of seller (Individual/Dealer/Trustmark Dealer)
  - `transmission`: Manual or Automatic
  - `owner`: Ownership history (First Owner, Second Owner, etc.)

---

## 🔍 Objectives

- 🧹 Clean and preprocess the data
- 📊 Explore data distributions and trends
- 🧠 Build a linear regression model to predict `km_driven`
- 📈 Evaluate model using R² score and cross-validation

---

## 🛠️ Tools & Libraries Used

- Python 3.x
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

---

## 🧪 Key Analysis Steps

### ✅ Data Cleaning & Transformation

- Removed the `name` column
- Calculated `Age` of cars: `Age = 2020 - year`
- Renamed and reorganized columns
- Checked for missing values (none found)
- Converted categorical features using `get_dummies()` for ML modeling

### ✅ Exploratory Data Analysis (EDA)

- Countplots for categorical variables (`fuel_type`, `seller_type`, etc.)
- Boxplots for numeric columns (`selling_price`, `km_driven`, `Age`)
- Distribution plots to examine skew and outliers

---

## 🧠 Model Building

- Model: **Linear Regression**
- Target: `km_driven`
- Features: All other cleaned and encoded columns
- Split: 80% training / 20% testing

```python
from sklearn.linear_model import LinearRegression
lr = LinearRegression()
car_pred_model(lr, "Linear_regressor.pkl")
````

---

## 📊 Model Evaluation

| Metric            | Score |
| ----------------- | ----- |
| 🧠 Train R² Score | 0.33  |
| 🧪 Test R² Score  | 0.29  |
| 🔁 CV Mean Score  | 0.33  |

> Residual analysis and `y_test vs y_pred_test` plots were also included.

---

## 📂 Folder Structure (Recommended)

```
used-car-analysis/
├── CAR DETAILS FROM CAR DEKHO.csv
├── car_analysis.ipynb
├── README.md
├── model/
│   └── Linear_regressor.pkl
└── plots/
    └── residual_plot.png
```

---

## ✨ Future Improvements

* Try more advanced models: RandomForest, XGBoost, or Gradient Boosting
* Feature engineering with text-based name/model column
* Include additional features like location, insurance status, etc.
* Deploy the model using Flask or Streamlit

---

## 👨‍💻 Author

**D. Lalith Kumar**
B.Tech CSE (AI & ML), VIT-AP University

---

## 📜 License

This project is open-source and intended for academic and educational use only. Please cite the original dataset source if used elsewhere.
