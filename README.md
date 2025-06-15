## 🧬 Breast Cancer Classification (Wisconsin Dataset)

This project performs classification on the **Breast Cancer Wisconsin (Diagnostic) Dataset** using multiple machine learning models, EDA techniques, and hyperparameter tuning. The goal is to predict whether a tumor is benign or malignant based on cell nucleus features.

---

### 📁 Dataset

* **Source**: UCI Machine Learning Repository
* **Instances**: 569 samples
* **Features**: 30 numeric features + ID + target (`diagnosis`: M = Malignant, B = Benign)

Key feature groups:

* `*_mean`: Mean of each measurement
* `*_se`: Standard error
* `*_worst`: Worst or largest measurement

---

### 📊 Exploratory Data Analysis (EDA)

* Analyzed feature correlations via heatmaps
* Identified multicollinearity and removed redundant features
* Visualized distributions of radius, texture, area, and other features
* Observed high correlation between radius, perimeter, and area

---

### 🧼 Preprocessing

* Label encoded `diagnosis` (M → 1, B → 0)
* Standardized features using `StandardScaler`
* Feature selection based on correlation thresholds
* Dropped highly correlated features for Logistic Regression and SVM Classifier

---

### 🧪 Models Used

* **Logistic Regression**
* **Support Vector Machine (SVC)**
* **Decision Tree**
* **Random Forest**
* **XGBoost Classifier**
* **Voting Classifier**
* **Stacking Classifier**
* **Multi-layer Stacking Classifier**

---

### 🔍 Hyperparameter Tuning

* Used `RandomizedSearchCV` for SVM tuning
* Parameters tuned: `C`, `gamma`, `kernel`
* Evaluated via 5-fold cross-validation
* Selected best estimator for final predictions

---

### 🧾 Evaluation

* Used:

  * Accuracy
  * Confusion Matrix
  * Classification Report (Precision, Recall, F1-score)
  * Analyzed generalization with learning curves

---

### 📌 Requirements

* Python 3.8+
* scikit-learn
* pandas, seaborn, matplotlib
* xgboost

Install via:

```bash
pip install numpy pandas matplotlib scipy scikit-learn seaborn xgboost
```
---

### ✅ Status

Project is in a complete, testable state. Final model achieves **high accuracy (\~95%)** on test data

---
## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [UCI Machine Learning Repository](https://archive.ics.uci.edu/) for providing the `Breast Cancer Diagnostic Dataset`
-` Scikit-learn` community for excellent machine learning tools
- Contributors and maintainers of all open-source libraries used in this project

---

⭐ If you found this project helpful, please consider giving it a star!