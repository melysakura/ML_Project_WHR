# 🌍 Predicting Country Happiness Levels Using Machine Learning

## 📌 Project Overview

This project was developed as part of the Ironhack Data Analytics Bootcamp Machine Learning module.

The objective was to build and evaluate machine learning models capable of predicting a country's happiness category (Low, Medium, or High) using socioeconomic indicators from the World Happiness Report.

Rather than predicting the exact Happiness Score, this project focuses on multiclass classification to identify countries' happiness levels based on measurable factors such as GDP, social support, life expectancy, freedom, generosity, and corruption.

---

## 🎯 Business Case

Imagine working as part of the analytics team supporting the World Happiness Report.

Before calculating the official Happiness Score, policymakers and researchers may want to estimate a country's happiness category using only available socioeconomic indicators.

This model provides a data-driven approach to classify countries into:

- Low Happiness
- Medium Happiness
- High Happiness

Such predictions could support policy analysis, resource allocation, and early assessment of countries where complete survey data may not yet be available.

---

## 📊 Dataset

Source:
World Happiness Report (2015–2019)

The dataset contains:

- 781 country-year observations
- 8 predictor variables
- 1 target variable

### Features

- Country
- Year
- GDP
- Social Support
- Life Expectancy
- Freedom
- Generosity
- Corruption

### Target Variable

The target variable was created by categorizing the Happiness Score into three meaningful classes:

| Category | Happiness Score |
|----------|-----------------|
| Low | < 4 |
| Medium | 4 – 6 |
| High | > 6 |

After creating the target, the original **Happiness Score** was removed from the predictors to prevent data leakage.

---

## 🧹 Data Preprocessing

The following preprocessing steps were performed:

- Missing value removal
- Train/Test Split (80/20)
- One-Hot Encoding of the Country variable
- Standardization of numerical variables using StandardScaler
- Feature selection through correlation analysis

---

## 🤖 Machine Learning Models

The following classification models were implemented and evaluated:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Bagging Classifier
- Random Forest
- Gradient Boosting
- AdaBoost

---

## 📈 Model Evaluation

Because the dataset is imbalanced, multiple evaluation metrics were used:

- Accuracy
- Precision
- Recall
- Average F1-score (Macro F1)
- Weighted F1-score
- Confusion Matrix

The Average F1-score was used to evaluate model performance equally across all happiness categories, while the Weighted F1-score considered the actual class distribution.

---

## ⚙️ Hyperparameter Tuning

The two best-performing models were further optimized using:

- GridSearchCV
- RandomizedSearchCV

Models tuned:

- Gradient Boosting
- Bagging Classifier

---

## 🏆 Results

| Model | Test Accuracy |
|--------|--------------:|
| Logistic Regression | 85.35% |
| K-Nearest Neighbors | 82.80% |
| Decision Tree | 82.17% |
| Bagging Classifier | 87.90% |
| Random Forest | 86.62% |
| Gradient Boosting | 88.54% |
| AdaBoost | 77.07% |

After hyperparameter tuning:

| Model | Tuning Method | Test Accuracy |
|--------|---------------|--------------:|
| Gradient Boosting | GridSearchCV | **89.81%** |
| Gradient Boosting | RandomizedSearchCV | **89.81%** |
| Bagging Classifier | GridSearchCV | 86.62% |
| Bagging Classifier | RandomizedSearchCV | 86.62% |

Gradient Boosting remained the best-performing model.

---

## 🔍 Feature Importance

The tuned Gradient Boosting model identified the most influential predictors as:

1. GDP
2. Freedom
3. Life Expectancy
4. Social Support
5. Corruption

GDP was by far the strongest predictor of national happiness.

---

## 💡 Conclusions

- Ensemble methods outperformed simpler classification algorithms.
- Gradient Boosting achieved the best balance between accuracy and generalization.
- Hyperparameter tuning improved the Gradient Boosting model but did not improve Bagging, illustrating that tuning does not always lead to better performance.
- Socioeconomic indicators alone provide strong predictive power for classifying national happiness levels.

---

## ⚠️ Limitations

- Small dataset (781 observations).
- Only five years of data.
- Limited socioeconomic variables.
- Happiness categories were manually defined.

Future work could include:

- Additional socioeconomic indicators
- Longer historical datasets
- Cross-validation with larger datasets

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook

---

## Link to Presentation

https://canva.link/guefctfhzcn8i0j

## 👩‍💻 Author

**Karen Melissa Sánchez Ramos**

Ironhack Data Analytics Bootcamp

GitHub: https://github.com/melysakura
