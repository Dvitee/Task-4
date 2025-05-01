# 🧠 Breast Cancer Classification using Logistic Regression

This project demonstrates the use of Logistic Regression for binary classification on the **Breast Cancer Wisconsin Dataset** using Scikit-learn. The goal is to understand model behavior under **realistic and constrained conditions**, such as limited training data and reduced feature set.

---

## 📂 Dataset

- **Source**: [UCI ML Repository - Breast Cancer Wisconsin Dataset](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic))
- **Target Variable**: `diagnosis` (Malignant = 1, Benign = 0)
- **Features Used**:
  - `texture_mean`
  - `smoothness_mean`
  - `symmetry_mean`

---

## 🧪 Task Objective

Build a binary classifier using logistic regression and evaluate its performance using key classification metrics:

1. Train-test split and basic preprocessing.
2. Fit a logistic regression model.
3. Evaluate using:
   - Confusion Matrix
   - Classification Report (Precision, Recall, F1)
   - ROC-AUC Curve
4. Explore the impact of threshold tuning and reduced feature sets.

---

## 🧾 Results Summary

### ✅ Confusion Matrix:





### ✅ Classification Report:
| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0 (Benign) | 0.70 | 0.85 | 0.76 | 71 |
| 1 (Malignant) | 0.61 | 0.40 | 0.48 | 43 |

- **Accuracy**: `0.675`
- **ROC AUC Score**: `0.77`

![ROC Curve](04a69a1d-b394-41fc-8a86-c8703a4a608a.png)

---

## 🔍 Observations

- The model performs better at predicting **benign cases** than malignant ones.
- **Recall for malignant cases is low (0.40)** — meaning many false negatives.
- ROC-AUC of **0.77** indicates moderate performance, better than random.
- High false negatives may be risky in medical diagnostics.

---

## ⚠️ Limitations

- **Limited feature set**: intentionally selected low-predictive features.
- **No feature scaling** applied.
- **Small training size** (only 20% of training data used).
- **Class imbalance** affected recall for the minority class.

---

## 🛠️ Future Improvements

- Use all informative features (e.g., `radius_mean`, `perimeter_mean`).
- Apply standardization using `StandardScaler`.
- Increase training size for better generalization.
- Tune threshold manually for improved sensitivity (recall).
- Apply class balancing techniques (`class_weight='balanced'`).

---

## 📌 Usage

```bash
# Clone this repo
git clone https://github.com/Dvitee/breast-cancer-logistic-regression.git
cd breast-cancer-logistic-regression

# Run in Jupyter Notebook or Colab

