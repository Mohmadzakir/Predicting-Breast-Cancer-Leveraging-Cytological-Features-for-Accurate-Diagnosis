# Predicting Breast Cancer: Leveraging Cytological Features for Accurate Diagnosis

## Project Overview
This project focuses on classifying breast tissue samples as **benign** or **malignant** using machine learning techniques. The study evaluates various **supervised** and **unsupervised** learning methods to identify key cytological features that aid in breast cancer diagnosis.

## Dataset
The analysis is conducted on the **BreastCancer** dataset, which contains **683 samples** with **10 features** describing cell characteristics, such as:
- Clump thickness (`Cl.thickness`)
- Cell size (`Cell.size`)
- Bare nuclei (`Bare.nuclei`)
- Epithelial cell size (`Epith.c.size`)
- Normal nucleoli (`Normal.nucleoli`)
- Other cytological attributes

The **target variable** (`Class`) labels samples as:
- **Benign (1)**
- **Malignant (2)**

## Methodology
### 1️⃣ Exploratory Data Analysis (EDA)
- **Data Cleaning:** Removing missing values, converting categorical variables, and normalizing features.
- **Distribution Analysis:** Generating histograms and summary statistics.
- **Feature Correlation:** Identifying relationships between predictors.
- **Unsupervised Learning:** Using **k-means clustering** to group similar samples.

### 2️⃣ Supervised Learning Approaches
1. **Logistic Regression (Subset Selection)** – Selects the most relevant predictors.
2. **LASSO Logistic Regression** – Uses L1 regularization to eliminate redundant features.
3. **Linear Discriminant Analysis (LDA)** – Classifies data using linear decision boundaries.
4. **Quadratic Discriminant Analysis (QDA)** – Captures non-linear class boundaries.

## Results
| **Model**                         | **Accuracy (%)** |
|------------------------------------|----------------|
| LASSO Logistic Regression         | **96.6**       |
| Subset Selection Logistic Regression | 96.1        |
| Linear Discriminant Analysis (LDA) | 95.6         |
| Quadratic Discriminant Analysis (QDA) | 95.6      |

- **LASSO Logistic Regression** outperformed other models, identifying key predictors:  
  `Cl.thickness`, `Cell.size`, `Bare.nuclei`, and `Bl.cromatin`.
- **Unsupervised learning (k-means clustering)** closely matched actual classifications, confirming the dataset’s strong structure.

## Key Insights
- **Cytological features** are crucial for breast cancer classification.
- **LASSO Regression** is the most effective approach due to its accuracy and interpretability.
- Some misclassifications occurred in **borderline cases**, suggesting potential improvements using **ensemble models** or **deep learning techniques**.


