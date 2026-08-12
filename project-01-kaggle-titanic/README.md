# Titanic - Machine Learning from Disaster 🚢

My submission for Kaggle's [Titanic: Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic) competition — predicting which passengers survived the sinking based on features like class, sex, age, and fare.

This was my first end-to-end ML project: cleaning real data, engineering features, training a model, and submitting predictions.

---

## 🎯 Goal

Given passenger data, predict whether each passenger survived (`1`) or did not (`0`).

---

## 🧹 Data Cleaning

- Filled missing **Age** values with the median age
- Filled missing **Embarked** values with the mode
- Dropped the **Cabin** column (too many missing values)
- Filled missing **Fare** values in the test set with the median

## 🔠 Feature Engineering

- Converted `Sex` to numeric (`male` → 0, `female` → 1)
- One-hot encoded `Embarked` into `Embarked_Q` / `Embarked_S`

**Features used for training:**
`Pclass`, `Sex`, `Age`, `SibSp`, `Parch`, `Fare`, `Embarked_Q`, `Embarked_S`

---

## 🤖 Model

- **Algorithm:** Decision Tree Classifier (`max_depth=3`)
- **Train/validation split:** 80/20
- **Validation accuracy:** **~80.4%**
- **Kaggle public leaderboard score:** **0.77990**
---

## 📁 Files

| File | Description |
|---|---|
| `titanic.ipynb` | Full notebook: data cleaning, feature engineering, model training, and prediction |
| `submission_file.csv` | Final predictions submitted to Kaggle (`PassengerId`, `Survived`) |

> Note: the raw `train.csv` / `test.csv` files aren't included here — download them from the [Kaggle competition page](https://www.kaggle.com/competitions/titanic/data) and place them in a `datasets/` folder to run the notebook.

---

## 📈 What I'd Improve Next

- Try other models (Random Forest, Logistic Regression) and compare accuracy
- Engineer new features (e.g. title extracted from `Name`, family size from `SibSp` + `Parch`)
- Use cross-validation instead of a single train/validation split
- Tune hyperparameters (e.g. `max_depth`, `min_samples_split`)

---

## 🛠️ Tools

`Python` · `pandas` · `numpy` · `scikit-learn`

---

⬅️ [Back to data-science-projects](../)
