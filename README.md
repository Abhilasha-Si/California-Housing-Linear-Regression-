# 🏠 California Housing Price Prediction
### Linear Regression Model | AI/ML Internship Task 1 — Maincrafts

---

## 📌 Project Overview
This project uses the **California Housing dataset** to predict median house values
using a **Linear Regression** model. It covers the complete ML workflow — from data
loading and exploratory data analysis (EDA) to model training, evaluation, and saving.

This project is part of **Task 1** of the AI/ML Internship at **Maincrafts**, designed
to introduce the full machine learning lifecycle in a short, reproducible project.

---

## 📁 Project Structure

```
📦 ml-linear-regression-california-housing
├── 📓 task1_ml_linear_regression.ipynb   ← Main Jupyter Notebook
├── 🤖 linear_model.pkl                   ← Saved trained model (Pickle)
├── 📋 ML_Linear_Regression_Report.pdf    ← Full project report (PDF)
├── 📄 requirements.txt                   ← All dependencies
└── 📄 README.md                          ← This file
```

---

## 📊 Dataset

- **Source:** California Housing Dataset (built into scikit-learn)
- **Origin:** 1990 U.S. Census data
- **Total Samples:** 20,640 rows
- **Input Features:** 8
- **Target Variable:** MedHouseVal (Median House Value in $100,000s)

| Feature       | Description                              |
|---------------|------------------------------------------|
| MedInc        | Median income in block group             |
| HouseAge      | Median house age in block group          |
| AveRooms      | Average number of rooms per household    |
| AveBedrms     | Average number of bedrooms               |
| Population    | Block group population                   |
| AveOccup      | Average household occupancy              |
| Latitude      | Block group latitude                     |
| Longitude     | Block group longitude                    |
| **MedHouseVal** | **Target — Median house value**        |

---

## 🔁 Steps Performed

1. **Data Loading** — Loaded dataset using `sklearn.datasets.fetch_california_housing`
2. **Exploratory Data Analysis (EDA)** — Checked shape, statistics, missing values
3. **Correlation Analysis** — Heatmap to find feature relationships
4. **Train-Test Split** — 80% training / 20% testing (`random_state=42`)
5. **Model Training** — Trained `LinearRegression` from scikit-learn
6. **Model Evaluation** — Measured MAE, RMSE, R² on test set
7. **Visualisation** — Actual vs Predicted scatter plot + Residuals histogram
8. **Model Saving** — Saved trained model using `pickle`

---

## 📈 Model Performance

| Metric   | Value  | Meaning                          |
|----------|--------|----------------------------------|
| MAE      | 0.533  | Average prediction error $53,300 |
| RMSE     | 0.746  | Penalises large errors more      |
| R² Score | 0.576  | Model explains 57.6% of variance |

> 💡 The most important feature is **MedInc** (Median Income) with a correlation of **+0.69** with house prices.

---

## 🛠️ Technologies Used

| Technology    | Purpose                          |
|---------------|----------------------------------|
| Python 3.x    | Programming language             |
| Pandas        | Data loading and manipulation    |
| NumPy         | Numerical operations             |
| Matplotlib    | Plotting and visualisation       |
| Seaborn       | Correlation heatmap              |
| Scikit-Learn  | ML model, metrics, data split    |
| Pickle        | Saving and loading the model     |
| Jupyter       | Interactive notebook environment |

---

## ▶️ How to Run

### 1. Clone the repository
```bash
git clone https://github.com/YOUR-USERNAME/ml-linear-regression-california-housing.git
cd ml-linear-regression-california-housing
```

### 2. Install all dependencies
```bash
pip install -r requirements.txt
```

### 3. Launch Jupyter Notebook
```bash
jupyter notebook task1_ml_linear_regression.ipynb
```

### 4. Run all cells from top to bottom ✅

---

## 🔄 Load the Saved Model (for Predictions)

```python
import pickle

# Load model
with open("linear_model.pkl", "rb") as f:
    model = pickle.load(f)

# Predict on new data
# new_data = [[MedInc, HouseAge, AveRooms, AveBedrms, Population, AveOccup, Lat, Long]]
prediction = model.predict([[3.5, 20, 5.0, 1.1, 800, 3.0, 34.0, -118.0]])
print(f"Predicted House Value: ${prediction[0]*100000:.2f}")
```

---

## 🚀 Improvement Ideas

- ✅ Feature Scaling using `StandardScaler`
- ✅ Try `Ridge` / `Lasso` Regression to reduce overfitting
- ✅ Use `Random Forest Regressor` for better accuracy
- ✅ Apply `Polynomial Features` to capture non-linear relationships
- ✅ Use `k-fold Cross Validation` for reliable evaluation
- ✅ Try `XGBoost` / `Gradient Boosting` for state-of-the-art performance

---

## 👤 Author

**[Your Name]**
AI/ML Internship — Maincrafts
📧 hr@maincrafts.com
🌐 [www.maincrafts.com](https://www.maincrafts.com)

---

## 📄 License

This project is created for educational purposes as part of an AI/ML Internship task at Maincrafts.
