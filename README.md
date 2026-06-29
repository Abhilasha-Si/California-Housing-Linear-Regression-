# 🤖 California Housing ML Internship Project
### Complete Machine Learning Workflow: Task 1, Task 2 & Task 3 | AI/ML Internship — Maincrafts

---

## 📌 Project Overview

This comprehensive project demonstrates the complete machine learning lifecycle using the **California Housing Dataset**. It covers three progressive tasks that build upon each other:

- **Task 1:** Linear Regression Model — Introduction to ML workflow
- **Task 2:** Model Comparison — Evaluating multiple algorithms
- **Task 3:** Model Validation & Hyperparameter Tuning — Professional ML practices

Each task increases in complexity and demonstrates industry-standard techniques for building production-ready machine learning models.

This project is part of the **AI/ML Internship at Maincrafts**, designed to provide hands-on experience with real-world machine learning workflows.

---

## 📁 Project Structure

```
📦 ml-california-housing-complete
│
├── 📂 Task-1_Linear_Regression
│   ├── 📓 Task1_ML_Linear_Regression.ipynb
│   ├── 🤖 linear_model.pkl
│   ├── 📋 Task1_Report_AbhilashaSingh.docx
│   └── 📄 README_Task1.md
│
├── 📂 Task-2_Model_Comparison
│   ├── 📓 Task2_Model_Comparison.ipynb
│   ├── 📋 Task2_Report_AbhilashaSingh.docx
│   └── 📄 README_Task2.md
│
├── 📂 Task-3_Validation_Tuning
│   ├── 📓 Task3_Validation_Tuning.ipynb
│   ├── 📋 Task3_Report_AbhilashaSingh.docx
│   ├── 📄 Task3_Complete_Guide.md
│   └── 📄 README_Task3.md
│
├── 📄 requirements.txt
└── 📄 README.md (← This file)
```

---

## 📊 Dataset Information

- **Source:** California Housing Dataset (built into scikit-learn)
- **Origin:** 1990 U.S. Census data
- **Total Samples:** 20,640 rows
- **Input Features:** 8
- **Target Variable:** HousePrice (Median House Value in $100,000s)

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
| **HousePrice** | **Target — Median house value**          |

---

## 🎯 Tasks Overview

### ✅ Task 1: Linear Regression Model

**Objective:** Build a basic linear regression model and understand the ML workflow.

**What You Learn:**
- Data loading and exploratory data analysis (EDA)
- Train-test split methodology
- Linear regression model training
- Model evaluation using MAE, RMSE, R²
- Model visualization and interpretation
- Saving and loading trained models

**Key Skills:**
- Data exploration and analysis
- Feature correlation analysis
- Matplotlib visualization
- Pickle model serialization

**Expected Outcomes:**
- Trained linear regression model
- Performance metrics (MAE, RMSE, R²)
- Correlation heatmap
- Actual vs Predicted scatter plot
- Residuals analysis

**File:** `Task1_ML_Linear_Regression.ipynb`

---

### ✅ Task 2: Model Comparison

**Objective:** Compare multiple regression algorithms to identify the best performer.

**What You Learn:**
- Feature scaling using StandardScaler
- Training multiple regression models:
  - Linear Regression (Baseline)
  - Ridge Regression (Regularized)
  - Decision Tree Regressor (Tree-based)
- Comprehensive model evaluation
- Performance comparison methodology
- Model selection criteria

**Key Skills:**
- Feature preprocessing and scaling
- Training multiple algorithms
- Comparative analysis
- Data visualization
- Performance metrics interpretation

**Expected Outcomes:**
- Three trained regression models
- Performance comparison table
- Best-performing model identification
- Visualization of model predictions
- Understanding of model trade-offs

**File:** `Task2_Model_Comparison.ipynb`

---

### ✅ Task 3: Model Validation & Hyperparameter Tuning

**Objective:** Build production-ready models using advanced validation techniques and systematic hyperparameter optimization.

**What You Learn:**
- Overfitting detection and control
- Cross-validation methodology (k-fold CV)
- Hyperparameter tuning with GridSearchCV
- Bias-variance tradeoff
- Model generalization and reliability
- Professional ML workflow practices

**Key Concepts:**
1. **Overfitting & Underfitting**
   - Detecting overfitting through train vs test performance
   - Gap between training and test RMSE indicates overfitting
   - Solutions: simpler models, constraints, more data

2. **Cross-Validation**
   - 5-fold cross-validation for reliable evaluation
   - Uses all data for training AND testing
   - Reduces luck/randomness from single split
   - Industry-standard practice

3. **Hyperparameter Tuning**
   - GridSearchCV for automated parameter search
   - Tests all combinations of specified values
   - Uses cross-validation for each combination
   - Automatically selects best parameters

4. **Model Generalization**
   - Ability to perform well on unseen data
   - More important than training accuracy
   - Verified through cross-validation
   - Essential for production deployment

**Implementation Steps:**
1. Data loading and preparation
2. Feature scaling (StandardScaler)
3. Train-test split (80-20)
4. Detect overfitting (unconstrained model)
5. Cross-validation (5-fold CV)
6. Hyperparameter tuning (GridSearchCV)
7. Optimized model evaluation
8. Baseline model training (Linear Regression, Ridge)
9. Model comparison summary
10. Final model selection justification

**Expected Outcomes:**
- Cross-validated performance scores
- Tuned model with controlled overfitting
- Comparison table with multiple models
- Clear justification for model selection
- Understanding of reliability vs accuracy tradeoff

**Files:** 
- `Task3_Validation_Tuning.ipynb` (Main code)
- `Task3_Complete_Guide.md` (Step-by-step guide)

---

## 📈 Model Performance Summary

### Task 1: Linear Regression

| Metric   | Value  | Meaning                          |
|----------|--------|----------------------------------|
| MAE      | 0.533  | Average prediction error $53,300 |
| RMSE     | 0.746  | Penalises large errors more      |
| R² Score | 0.576  | Model explains 57.6% of variance |

**Key Finding:** Median Income (MedInc) is the strongest predictor (correlation: +0.69)

---

### Task 2: Model Comparison

| Model                   | RMSE  | R² Score | Observation                |
|-------------------------|-------|----------|---------------------------|
| Linear Regression       | 0.746 | 0.576    | Baseline model             |
| Ridge Regression        | 0.742 | 0.580    | Slightly better than Linear|
| Decision Tree Regressor | 0.690 | 0.615    | Best performer             |

**Conclusion:** Decision Tree model outperforms linear models due to capturing non-linear relationships.

---

### Task 3: Model Validation & Tuning

| Model                      | RMSE  | R² Score | Cross-Validation Status |
|----------------------------|-------|----------|------------------------|
| Linear Regression          | 0.746 | 0.576    | Baseline                |
| Ridge Regression           | 0.742 | 0.580    | Task-2 reference        |
| **Tuned Decision Tree** ✓  | 0.712 | 0.603    | **Best & Most Reliable**|

**Key Achievement:** 
- Controlled overfitting through hyperparameter constraints
- Achieved consistent cross-validation performance
- Model generalizes well to unseen data
- Production-ready reliability

---

## 🛠️ Technologies & Libraries Used

| Technology    | Purpose                                      |
|---------------|----------------------------------------------|
| Python 3.x    | Core programming language                    |
| Pandas        | Data loading, manipulation, analysis         |
| NumPy         | Numerical computations                       |
| Matplotlib    | Static visualizations and plots              |
| Seaborn       | Statistical visualizations (heatmaps)        |
| Scikit-Learn  | ML models, metrics, preprocessing             |
| StandardScaler| Feature normalization                        |
| GridSearchCV  | Hyperparameter optimization                  |
| Cross-validation | Reliable model evaluation                  |
| Pickle        | Model serialization and saving               |
| Jupyter       | Interactive notebook environment              |

---

## ▶️ How to Run All Tasks

### Prerequisites

```bash
# Python 3.7 or higher
python --version

# pip package manager
pip --version
```

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/ml-california-housing-complete.git
cd ml-california-housing-complete
```

### 2. Create Virtual Environment (Optional but Recommended)

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open and Run Notebooks

**For Task 1:**
```bash
jupyter notebook Task-1_Linear_Regression/Task1_ML_Linear_Regression.ipynb
```

**For Task 2:**
```bash
jupyter notebook Task-2_Model_Comparison/Task2_Model_Comparison.ipynb
```

**For Task 3:**
```bash
jupyter notebook Task-3_Validation_Tuning/Task3_Validation_Tuning.ipynb
```

### 6. Run All Cells

Execute all notebook cells from top to bottom (Kernel → Run All)

---

## 💻 Quick Code Examples

### Loading and Using Task 1 Model

```python
import pickle
import pandas as pd
from sklearn.datasets import fetch_california_housing

# Load the saved model
with open("Task-1_Linear_Regression/linear_model.pkl", "rb") as f:
    model = pickle.load(f)

# Prepare new data (8 features)
new_data = [[3.5, 20, 5.0, 1.1, 800, 3.0, 34.0, -118.0]]

# Make prediction
prediction = model.predict(new_data)
predicted_price = prediction[0] * 100000  # Convert to actual price

print(f"Predicted House Value: ${predicted_price:,.2f}")
```

### Task 2 Model Comparison

```python
from sklearn.linear_model import LinearRegression, Ridge
from sklearn.tree import DecisionTreeRegressor
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import mean_squared_error, r2_score

# Load and prepare data
data = fetch_california_housing(as_frame=True)
X = data.data
y = data.target

# Scale features
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

# Train-test split
X_train, X_test, y_train, y_test = train_test_split(
    X_scaled, y, test_size=0.2, random_state=42
)

# Train models
models = {
    'Linear Regression': LinearRegression(),
    'Ridge Regression': Ridge(alpha=1.0),
    'Decision Tree': DecisionTreeRegressor(random_state=42)
}

# Evaluate
results = {}
for name, model in models.items():
    model.fit(X_train, y_train)
    y_pred = model.predict(X_test)
    rmse = np.sqrt(mean_squared_error(y_test, y_pred))
    r2 = r2_score(y_test, y_pred)
    results[name] = {'RMSE': rmse, 'R²': r2}

# Display results
results_df = pd.DataFrame(results).T
print(results_df)
```

### Task 3 Cross-Validation & Tuning

```python
from sklearn.model_selection import cross_val_score, GridSearchCV
from sklearn.tree import DecisionTreeRegressor

# Cross-validation
cv_scores = cross_val_score(
    DecisionTreeRegressor(random_state=42), 
    X_scaled, y, 
    scoring="neg_root_mean_squared_error",
    cv=5
)

print(f"CV RMSE Mean: {-cv_scores.mean():.4f}")
print(f"CV RMSE Std: {cv_scores.std():.4f}")

# Hyperparameter tuning
param_grid = {
    "max_depth": [3, 5, 7, 10],
    "min_samples_split": [2, 5, 10]
}

grid = GridSearchCV(
    DecisionTreeRegressor(random_state=42),
    param_grid,
    scoring="neg_root_mean_squared_error",
    cv=5
)

grid.fit(X_train, y_train)

print(f"Best Parameters: {grid.best_params_}")
print(f"Best CV Score: {-grid.best_score_:.4f}")
```

---

## 📊 Key Learnings Across All Tasks

### From Task 1:
- ✅ Complete ML workflow from data to model
- ✅ Feature correlation and importance
- ✅ Model evaluation metrics (MAE, RMSE, R²)
- ✅ Model persistence with Pickle

### From Task 2:
- ✅ Importance of feature scaling
- ✅ Comparing multiple algorithms
- ✅ Objective model selection criteria
- ✅ Understanding algorithm trade-offs

### From Task 3:
- ✅ Detecting and controlling overfitting
- ✅ Cross-validation for reliable evaluation
- ✅ Automated hyperparameter optimization
- ✅ Model reliability vs accuracy balance
- ✅ Professional ML best practices
- ✅ Production-ready model development

---

## 🚀 Next Steps & Improvements

### Beginner Level:
- ✅ Add more visualization types
- ✅ Experiment with different train-test splits
- ✅ Try different scaling methods

### Intermediate Level:
- ✅ Feature engineering (polynomial features)
- ✅ Random Forest Regressor
- ✅ Gradient Boosting Regressor
- ✅ XGBoost implementation
- ✅ Ensemble methods
- ✅ Stacking and Blending

### Advanced Level:
- ✅ Deep learning (Neural Networks)
- ✅ Time series forecasting extensions
- ✅ Automated ML (AutoML)
- ✅ Model interpretation (SHAP, LIME)
- ✅ Production deployment (Flask, Docker)
- ✅ Model monitoring and retraining

---

## 📋 Report Files

Each task includes a professional report:

1. **Task1_Report_AbhilashaSingh.docx**
   - Project overview
   - EDA results
   - Model performance
   - Conclusions

2. **Task2_Report_AbhilashaSingh.docx**
   - Model comparison methodology
   - Performance metrics
   - Algorithm analysis
   - Best model justification

3. **Task3_Report_AbhilashaSingh.docx**
   - Overfitting analysis
   - Cross-validation results
   - Hyperparameter tuning outcomes
   - Model selection justification
   - Industry best practices

---

## ✅ Submission Checklist

### For Each Task:
- [ ] Jupyter Notebook with all code executed
- [ ] Generated report (.docx file)
- [ ] All visualizations working
- [ ] Model performance metrics documented
- [ ] Clear explanations and comments in code

### Final Submission:
- [ ] All three tasks completed
- [ ] Three notebooks with executed code
- [ ] Three professional reports
- [ ] requirements.txt with all dependencies
- [ ] This comprehensive README

---

## 🛠️ Requirements File

Create `requirements.txt` with:

```
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
scikit-learn>=1.0.0
jupyter>=1.0.0
jupyter-notebook>=6.4.0
```

Install with:
```bash
pip install -r requirements.txt
```

---

## 👤 Author

**Abhilasha Singh**
- AI/ML Internship — Maincrafts
- 📧 hr@maincrafts.com
- 🌐 [www.maincrafts.com](https://www.maincrafts.com)

---

## 📞 Support & Questions

If you have questions about:
- **Task 1:** Review data loading and model training concepts
- **Task 2:** Check feature scaling and model comparison methodology
- **Task 3:** Refer to `Task3_Complete_Guide.md` for step-by-step code examples

---

## 📄 License

This project is created for educational purposes as part of the AI/ML Internship Program at Maincrafts. All rights reserved.

---

## 🎓 Learning Path

```
START
  ↓
Task 1: Build basic ML model → Understand workflow
  ↓
Task 2: Compare algorithms → Learn model selection
  ↓
Task 3: Validate & tune → Master professional practices
  ↓
PROFICIENCY IN ML DEVELOPMENT ✓
```

---

## 📌 Important Notes

1. **Reproducibility:** Always use `random_state=42` for consistent results
2. **Data Split:** Always split before scaling to prevent data leakage
3. **Cross-Validation:** Essential for reliable performance estimates
4. **Documentation:** Write clear code comments explaining your approach
5. **Version Control:** Commit changes regularly with meaningful messages

---

## 🎯 Success Criteria

### Task 1 ✓
- [x] Linear model trained successfully
- [x] Performance metrics calculated
- [x] Model saved to pickle file
- [x] Report generated

### Task 2 ✓
- [x] Three models trained and compared
- [x] Performance metrics for each model
- [x] Clear model selection justification
- [x] Visualizations created

### Task 3 ✓
- [x] Overfitting detected and analyzed
- [x] 5-fold cross-validation implemented
- [x] GridSearchCV hyperparameter tuning completed
- [x] Final model selection justified
- [x] Report documenting best practices

---

**Last Updated:** June 29, 2026
**Status:** Complete ✅
**Difficulty:** Beginner → Intermediate → Advanced
