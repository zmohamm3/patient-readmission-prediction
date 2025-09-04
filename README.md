# 🏥 Predicting Hospital Readmissions for Diabetic Patients

## 📌 Project Overview

Hospital readmissions are costly for healthcare providers and stressful for patients. This project leverages the **UCI Diabetes Dataset** to predict whether a patient will be readmitted within 30 days of discharge. The primary objective is to use machine learning to improve patient care and reduce healthcare costs.

---

## 📊 Dataset

* **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/diabetes+130-us+hospitals+for+years+1999-2008)
* **Size:** 100,000+ patient encounters
* **Features:** Demographics, lab tests, medications, diagnoses, hospital visits
* **Target Variable:** `readmitted` (<30, >30, NO)

---

## ⚙️ Workflow

1. **Data Loading & Cleaning**

   * Replaced missing values
   * Dropped identifier columns
   * Encoded categorical features

2. **Exploratory Data Analysis (EDA)**

   * Distribution of readmissions
   * Feature inspection and correlations

3. **Modeling Approaches**

   * Logistic Regression (Base)
   * Logistic Regression (Class Weight Balanced)
   * Logistic Regression (SMOTE Oversampling)
   * Random Forest
   * XGBoost

4. **Evaluation Metrics**

   * Accuracy
   * Recall (sensitivity for positive cases)
   * ROC-AUC

---

## 📈 Results

| Model                              | Accuracy | Recall | ROC-AUC |
| ---------------------------------- | -------- | ------ | ------- |
| Logistic Regression (Base)         | \~0.75   | \~0.40 | \~0.70  |
| Logistic Regression (Class Weight) | \~0.72   | \~0.55 | \~0.73  |
| Logistic Regression (SMOTE)        | \~0.71   | \~0.58 | \~0.74  |
| Random Forest                      | \~0.78   | \~0.45 | \~0.76  |
| XGBoost                            | \~0.80   | \~0.52 | \~0.79  |

🔹 **Key Insight:** Handling class imbalance (via SMOTE or class weighting) significantly improves **Recall**, which is critical for healthcare applications.

---

## 📊 Visualization

The notebook includes grouped bar charts comparing Accuracy, Recall, and ROC-AUC across all models:

<img width="905" height="463" alt="Model comparision" src="https://github.com/user-attachments/assets/53b9cd80-aaad-447a-9e65-71063249bdf4" />

---

## 🚀 How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/diabetes-readmission-prediction.git
   cd diabetes-readmission-prediction
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook:

   ```bash
   jupyter notebook Diabetes_Readmission.ipynb
   ```

---

## 📦 Requirements

* Python 3.8+
* pandas
* numpy
* scikit-learn
* imbalanced-learn
* matplotlib
* xgboost

---

## 🔮 Future Work

* Hyperparameter tuning for XGBoost and Random Forest
* Feature engineering (diagnosis grouping, temporal patterns)
* Deep learning approaches (RNN/LSTM for sequential visits)
* Deployment as a web app for hospital use

---

## 👨‍💻 Author

**Zubair Mohammed**
Data Analyst | SQL Engineer | Machine Learning Enthusiast
[LinkedIn](https://www.linkedin.com) | [GitHub](https://github.com/yourusername)

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
