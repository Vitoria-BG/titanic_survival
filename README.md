# Titanic - Machine Learning from Disaster 🚢

This repository presents a machine learning solution for the classic Titanic Kaggle competition. The project implements an **Ensemble Model**.

### 📈 Performance
**Kaggle Score:** `0.77751`  
**Model Type:** Ensemble (Voting Classifier: SVM + Random Forest)

***

### ⚙️ Project Workflow

1.  **Data Cleaning & Feature Engineering:**
    * `Cabin` was disregarded because it had more than 75% null values.
    * Handled missing values for `Age`, `Fare`, and `Embarked`.
    * Created `TitleGroup` extracted from passenger names.
    * Engineered `Family` size and `AgeGroup` bins.

3.  **Model Training & Selection:**
    * Utilized Cross-Validation to ensure model stability.
    * Utilized GridSearchCV to find the best hyperparameter combinations for each ML algorithm.
    * Combined **Support Vector Machine (SVM)** and **Random Forest**.
    * Saved model artifacts using `joblib` for reproducibility.

4.  **Inference & Validation:**
    * Final predictions on the `x_test.csv` set.
    * Sanity check on survival distribution (38% predicted survival rate).
    * Validation of historical logic (survival rates highly correlated with gender and class).

***

### 🛠️ Technologies & Tools

* **Python**: Main programming language.
* **Pandas**: Data manipulation and analysis.
* **NumPy**: Numerical computing.
* **Scikit-Learn**: Ensemble, GridSearchCV, ML algorithms, Metrics.
* **Joblib**: Model persistence and serialization.
* **Matplotlib / Seaborn**: EDA and feature importance visualization.
* **Jupyter Notebook**: Modular development and documentation.
* **Git/GitHub**: Version control.
* **Kaggle API/Platform**: Competition hosting and submission.
  
***

### 📁 Repository Structure

```text
├── data/                           # Raw and processed datasets
├── models/                         # Saved .joblib final model artifacts
└── notebooks/                      # Modularized development steps
    ├── 01_EDA_and_Data_Cleaning    # Data understanding, EDA and Preprocessing
    ├── 02_Model_Selection          # Model training and analysis
    └── 03_Model_Testing            # Prediction and final submission
