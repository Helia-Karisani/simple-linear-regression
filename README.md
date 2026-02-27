

# 📈 Simple Linear Regression

This project implements a **simple linear regression model** to study the relationship between **engine size** and **CO₂ emissions** using a real-world vehicle dataset.

The goal is to walk through the **entire machine learning pipeline** step by step, from data exploration to model evaluation and visualization.

---

## 🧠 Project Overview

We model the relationship:

**CO₂ Emissions = f(Engine Size)**

This is a **univariate regression problem**, where:
- Input feature (X): `ENGINESIZE`
- Target variable (y): `CO2EMISSIONS`

---

## 📂 Dataset

The dataset contains vehicle specifications, including:
- Engine size
- Number of cylinders
- Fuel consumption
- CO₂ emissions

After initial inspection, we select a subset of relevant features for analysis.

---

## 🧹 Data Preparation

We extract the required columns and convert them into NumPy arrays:

- `X`: Engine size values
- `y`: Corresponding CO₂ emission values

Each row represents **one vehicle**, and the pairing between `X[i]` and `y[i]` is preserved by index.

---

## 🔀 Train–Test Split

The dataset is randomly split into:

- **80% training data**
- **20% testing data**

### Important concepts:
- Training data is used to **learn** the model parameters
- Testing data is **never seen during training**
- Testing data is used **only for evaluation**

This helps measure how well the model generalizes to unseen data.

---

## 🏋️ Model Training

We train a **Simple Linear Regression** model using scikit-learn.

- The model learns:
  - `coef_` → slope of the regression line
  - `intercept_` → y-intercept

The model equation is:

```

y = coef_ * x + intercept_

```

Although `X` contains only one feature, it is reshaped into a **2D array** because scikit-learn expects inputs in the form:

```

(n_samples, n_features)

```

---

## 🔮 Prediction

After training, we use the model to make predictions on the **test dataset**:

- Input: `X_test`
- Output: `y_pred` (predicted CO₂ emissions)

These predictions represent what the model estimates for **previously unseen vehicles**.

---

## 📏 Model Evaluation

We evaluate model performance using standard regression metrics:

- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **R² Score**

Important clarification:

Although the **training and test sets are disjoint**, we still compute error by comparing:
- `y_test` → true CO₂ values (known but hidden from training)
- `y_pred` → model predictions

This comparison measures **generalization performance**, not training accuracy.

---

## 📊 Visualization

We visualize the results using Matplotlib:

- **Scatter plot** of the test data points
- **Regression line** using learned `coef_` and `intercept_`

This plot shows how well the learned linear relationship fits unseen data.

---

## 🧪 Key Takeaways

- Linear regression learns a global relationship from training data
- Testing data evaluates how well the model generalizes
- Even with one feature, inputs must be shaped correctly
- Errors are computed between predictions and known test labels
- Visualization helps interpret model behavior intuitively

---

## 🛠️ Technologies Used

- Python
- NumPy
- Pandas
- scikit-learn
- Matplotlib
- Jupyter Notebook

---

## 📌 Notes

This project is intended for **learning and demonstration purposes**, focusing on clarity and conceptual understanding rather than model optimization.
```

