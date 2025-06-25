# 📊 Logistic Regression: Predicting Exam Results

This project uses **logistic regression** to predict whether a student will pass or fail based on two key factors:

- Hours Studied
- Hours Slept

The data is **synthetically generated** and contains 100 examples with added noise to simulate real-world variation.

---

## 📁 Project Files

- `logistic_regression_student.ipynb` – Jupyter Notebook with full code
- `README.md` – This file
- (Optional) `requirements.txt` – Package dependencies

---

## 🔧 Tools & Libraries

- Python 3
- pandas
- numpy
- matplotlib
- scikit-learn

---

## 🧠 Project Highlights

- Generate synthetic student performance data
- Train a logistic regression model
- Visualize input data and model predictions
- Predict the outcome for new data points
- Explore model probabilities using `predict_proba`

---

## 📈 Dataset Overview

| Column         | Description                            |
|----------------|----------------------------------------|
| Hours_Studied  | Integer from 1 to 12                   |
| Hours_Slept    | Inversely related to study hours       |
| Passed         | 1 if passed, 0 if failed (with noise)  |

---

## 🧪 Example: Predict a New Student

```python
specific_study = 7
specific_sleep = 3
new_data_point = pd.DataFrame({'Hours_Studied': [specific_study], 'Hours_Slept': [specific_sleep]})
prediction = model.predict(new_data_point)

print("Prediction:", "Passed" if prediction[0] == 1 else "Failed")
