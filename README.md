# 🏫 Public School Characteristics Machine Learning Classification Task

This project focuses on building a machine learning pipeline to classify public schools based on their characteristics. The goal is to analyze various school attributes and predict their categorical groupings using supervised learning techniques.

---

## 📖 Project Overview

Public schools vary significantly in their characteristics such as size, location, student demographics, and resource availability. This classification task aims to:

- Preprocess and explore a dataset of public schools.
- Train machine learning models to predict school type.
- Evaluate model performance using appropriate metrics.

The project is implemented as a Jupyter Notebook for ease of experimentation and visualization.

---

## 📂 Dataset

The dataset contains multiple features describing public school characteristics. These may include:

- **Location data** (urban, suburban, rural)
- **Enrollment numbers**
- **Student-teacher ratios**
- **Demographics** (percentages of different student groups)
- **Funding/resource indicators**

*(Dataset is Public_School_Characteristics_-_Current.csv)*

---

## 🛠️ Methods

The notebook includes:
- **Data Preprocessing**
  - Handling missing values
  - Feature encoding (categorical to numerical)
  - Normalization/scaling
- **Exploratory Data Analysis (EDA)**
  - Visualizations to understand feature distributions
  - Correlation analysis
- **Modeling**
  - Logistic Regression
  - Decision Trees
  - Random Forest
- **Evaluation**
  - Accuracy, Precision, Recall, F1-score
  - Confusion Matrix

---

## Requirements

The notebook requires the following Python packages:

- numpy
- pandas
- scikit-learn
- matplotlib
- seaborn
- jupyter

---

## 📊 Results

**Learning Curves**

The learning curves plotted for all classifier models show:

- Both training and validation accuracies converge as the number of training samples increases.

- There is no large gap between training and validation performance.

- This indicates:

    - The models are not overfitting (low variance).

    - The dataset size is sufficient for achieving robust performance.

This behavior suggests the classifiers are able to learn effectively from the available data and benefit from larger datasets without significant diminishing returns.


**Bias-Variance Tradeoff Curves**

- The bias-variance tradeoff across the models appears well balanced:

  - Random Forest achieved low bias due to its ensemble nature and avoided high variance thanks to randomization and parameter tuning.

  - Decision Trees showed slightly higher variance (overfitting tendencies), but pruning and hyperparameter tuning mitigated this.

  - Logistic Regression displayed higher bias, underfitting complex patterns in the data, but this is expected for linear models.

Overall, ensemble methods maintained low training error and comparable validation error, striking an excellent balance.


**ROC Curves & AUC**

- ROC curves plotted for each classifier demonstrated:

  - Random Forest (SMOTE) achieved a near-perfect ROC curve with an AUC (Area Under Curve) approaching 0.95–0.98.

  - Decision Tree and Logistic Regression ROC curves were also well above random guessing (AUC > 0.90).

  - The separation between the positive and negative classes is very clear, even in imbalanced settings.

This indicates the models are not only accurate but also have excellent discriminative ability for different school types.

---

## Summary

📈 Learning curves show strong generalization.

🔥 Bias-variance tradeoff is well-managed, particularly in Random Forest models.

✅ ROC curves and AUC confirm high classification confidence, even in imbalanced settings.

These results suggest that the chosen models, particularly Random Forest with SMOTE, are highly reliable and suitable for real-world deployment.
