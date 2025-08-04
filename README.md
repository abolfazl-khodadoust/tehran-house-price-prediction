# 🏠 Tehran House Price Prediction

This project aims to predict housing prices in Tehran using a variety of machine learning algorithms and feature engineering techniques. It includes data preprocessing, visualization, model training, and evaluation.

---

## 📂 Project Structure

- `House_Pred.ipynb`: The main Jupyter notebook containing the full workflow, from data loading to model comparison.
- `HousePrice-new.csv`: The dataset used for model training and evaluation.

---

## 📊 Dataset Description

The dataset contains housing features in Tehran, including:

- `Area`: The size of the property in square meters
- `Room`: Number of rooms
- `Parking`: Availability of parking (1 or 0)
- `Elevator`: Elevator availability (1 or 0)
- `Warehouse`: Availability of a warehouse/storage (1 or 0)
- `Address`: Location as a categorical feature
- `Price`: (Target) The final price of the house in local currency (removed from features during training)

---

## ⚙️ Workflow Summary

1. **Data Cleaning**
   - Dropped rows with missing values
   - Removed outliers using Z-score filtering
   - Converted boolean features (`Parking`, `Elevator`, `Warehouse`) to integers

2. **Feature Engineering**
   - One-hot encoding for the `Address` column
   - Feature scaling with `StandardScaler`

3. **Modeling**
   Applied and compared multiple ML models:
   - `Linear Regression` (via SGD)
   - `Decision Tree Regressor`
   - `Random Forest Regressor`
   - `Support Vector Regressor (SVR)`

4. **Model Evaluation**
   - Metrics: R² Score, Mean Squared Error (MSE)
   - Visual comparison of predicted vs. actual prices
   - Feature importance via permutation importance and decision tree visualization


## 📈 Results

- The **Random Forest Regressor** performed the best in terms of R² score.
- Feature importance analysis revealed that `Area` and `Address` were among the most impactful features.

---

## 📌 Requirements

Install dependencies using:

```bash
pip install -r requirements.txt
````

Main libraries used:

* `pandas`
* `numpy`
* `matplotlib`, `seaborn`
* `scikit-learn`
* `scipy`
* `pydotplus` (for tree visualization)

---

## 🚀 How to Run

1. Clone this repository:

```bash
git clone https://github.com/abolfazl-khodadoust/tehran-house-price-prediction.git
cd tehran-house-price-prediction
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the notebook:

```bash
jupyter notebook House_Pred.ipynb
```

---

## 📌 Notes

* Ensure the dataset (`HousePrice-new.csv`) is in the same directory as the notebook.
* If `pydotplus` or `graphviz` visualization fails, install `graphviz` system-wide and add it to your PATH.

---
