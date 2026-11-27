# Machine Learning & Deep Learning 🤖

Beginner-friendly, hands-on notebooks for learning Machine Learning and Deep Learning from scratch. Every notebook starts with the core idea in plain language and then builds it in Python, one cell at a time, with an explanation for each step.

These notebooks were created for the **AI for Everyone** students, but anyone starting out with ML can follow along. No prior ML experience needed. Basic Python helps.

> 🗣️ Explanations inside the notebooks are written in simple **Urglish** (Roman Urdu mixed with English) so they're easy to follow for learners in Pakistan.

---

## 📚 Notebooks

| # | Topic | Type | Dataset | Open |
|---|---|---|---|---|
| 1 | [Linear Regression](linear_regression) | Regression | `Housing.csv` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/azm-ai/Machine-learning-Deep-Learning/blob/main/linear_regression/Linear_Regression_Housing_AI_for_Everyone.ipynb) |
| 2 | [Polynomial Regression](Polynomial_regression) | Regression | `Salary_Data.csv` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/azm-ai/Machine-learning-Deep-Learning/blob/main/Polynomial_regression/Polynomial_Regression_Salary_AI_for_Everyone.ipynb) |
| 3 | [Logistic Regression](logistic_regression) | Classification | `diabetes.csv` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/azm-ai/Machine-learning-Deep-Learning/blob/main/logistic_regression/Logistic_Regression_Diabetes_AI_for_Everyone.ipynb) |
| 4 | [KNN Classifier](knn_classifier) | Classification | `diabetes.csv` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/azm-ai/Machine-learning-Deep-Learning/blob/main/knn_classifier/KNN_Classifier_Diabetes_AI_for_Everyone.ipynb) |

More topics will be added over time.

---

## 🗂️ What each notebook covers

### 1. Linear Regression: House price prediction 🏠
- What Machine Learning and Supervised Learning are
- Simple Linear Regression (area only) vs Multiple Linear Regression (all features)
- Encoding yes/no and categorical columns
- Evaluation with MAE, RMSE and R², and predicting the price of a new house
- **Result:** R² goes from 0.27 (area only) to 0.65 (all features)

### 2. Polynomial Regression: Salary prediction 💼
- Fitting curves instead of straight lines with `PolynomialFeatures`
- Real-world cleaning: missing values, ~4,900 duplicate rows, inconsistent category names
- Ordinal vs one-hot encoding, and feature engineering from job titles
- Underfitting vs overfitting, feature scaling, Pipelines, and choosing the degree with Cross Validation
- Epochs, batches, learning rate and loss, shown live with `SGDRegressor`
- **Result:** test R² of 0.80 (vs 0.72 for plain Linear Regression), model exported as a `.pkl`

### 3. Logistic Regression: Diabetes prediction 🩺
- Classification vs regression, and the Sigmoid function
- Hidden missing values (impossible zeros in Glucose, BMI, etc.) filled with the median inside a Pipeline to avoid data leakage
- Class imbalance and `stratify`
- Confusion Matrix, Precision, Recall, F1 and ROC/AUC, and why accuracy alone can mislead
- Tuning `C` and understanding `max_iter`
- Lowering the decision threshold to catch more patients (Recall goes from 50% to 80%)
- **Result:** model and threshold exported as a `.pkl`

### 4. KNN Classifier: Diabetes prediction 🏘️
- How K-Nearest Neighbors works, with a hand-calculated demo
- Euclidean distance and why KNN is a "lazy learner"
- Why scaling is essential for KNN (accuracy goes from 67.5% to 75.3% with scaling alone)
- Decision boundaries for K = 1, 15 and 201 to see overfitting and underfitting
- Choosing K with Cross Validation, and `uniform` vs `distance` weights
- Head-to-head comparison with Logistic Regression
- Viewing a new patient's actual nearest neighbors from the saved model

> ⚠️ The diabetes notebooks are for learning only. A real diagnosis needs a doctor and lab tests.

---

## 🚀 How to Run

### Option 1: Google Colab (easiest, nothing to install)
1. Click the **Open in Colab** badge for any notebook in the table above
2. In the data-loading cell, uncomment the two upload lines and run it
3. Upload the CSV file from the same folder in this repo
4. Run the cells top to bottom with `Shift + Enter`

### Option 2: On your own computer
```bash
git clone https://github.com/azm-ai/Machine-learning-Deep-Learning.git
cd Machine-learning-Deep-Learning
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook
```
Open any folder, then the notebook inside it. Each folder already has its CSV next to the notebook.

> 🔒 The `.pkl` files are trained models saved with `pickle`. Only load pickle files from sources you trust, and use a similar `scikit-learn` version to the one they were saved with.

---

## 🛠️ Tech Stack
- **Python 3**
- **pandas** and **numpy** for data handling
- **matplotlib** and **seaborn** for charts
- **scikit-learn** for models, preprocessing, pipelines and metrics

---

## 👨‍🏫 Author

**Mian Muhammad Azam Ayaz**
CEO & Co-founder, TenH Tech | AI, GFX and Marketing mentor based in Lahore, Pakistan

- Personal brand: **@mianazam.ai**
- LinkedIn: [mian-azam](https://www.linkedin.com/in/mian-azam/)
- Email: azamwithai@gmail.com
- GitHub: [@azm-ai](https://github.com/azm-ai)

If these notebooks helped you, give the repo a ⭐ and share it with someone who's starting their AI journey.
