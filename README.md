# Credit Risk Analysis Project

## Overview

This repository contains a comprehensive credit risk analysis project using machine learning techniques. The project aims to predict loan defaults using the Lending Club dataset, employing various data preprocessing techniques, sampling methods to handle class imbalance, and multiple modeling approaches.

## Project Structure

```
├── data/                  # Data directory
│   └── README.md          # Data documentation and usage instructions
├── notebooks/             # Jupyter notebooks
│   └── Final_project.ipynb  # Main analysis notebook
├── requirements.txt       # Python package dependencies
└── README.md              # Project documentation
```

## Installation

```bash
# Clone the repository
git clone https://github.com/LIULIMENG717/ST5188_Project.git
cd ST5188_project

# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows, use: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

## Data

### Data Source

The data used in this project comes from the Lending Club Company public database and is available on Kaggle: [Loan - Credit Risk & Population Stability](https://www.kaggle.com/datasets/beatafaron/loan-credit-risk-and-population-stability?select=loan_2014_18.csv).

### Dataset Description

The dataset is divided into two parts:

1. **loan_2014-2018.csv**: Contains almost 1,800,000 consumer loans issued from 2014 to 2018.
2. **loan_2019-2020.csv**: Separate data to validate if the model has similar characteristics and is still up to date.

Note: I only use `loan_2014-2018.csv`.

LendingClub is a US peer-to-peer lending company headquartered in San Francisco, California. It was the first peer-to-peer lender to register its offerings as securities with the Securities and Exchange Commission (SEC) and to offer loan trading on a secondary market. LendingClub is the world's largest peer-to-peer lending platform.

### Data Handling

Due to the large size of the dataset, it is not included in this repository. Please download it directly from the Kaggle link above and place it in the `data/` directory before running the notebook.

## Usage

1. Download the dataset from Kaggle and place it in the `data/` directory
2. Ensure you have installed all dependencies as described above
3. Open the Jupyter notebook in the `notebooks/` directory:

```bash
jupyter notebook notebooks/Final_project.ipynb
```

## Project Pipeline

The analysis in `Final_project.ipynb` follows this methodology:

### 1. Data Preprocessing

- Dealing with missing values
- Data cleaning and transformation

### 2. Exploratory Data Analysis (EDA)

- Statistical analysis
- Data visualization
- Feature relationships and distributions

### 3. Dimensionality Reduction

- Principal Component Analysis (PCA)

### 4. Handling Class Imbalance

Comparison of various sampling methods:

- **Under-Sampling**: Tomek-Links
- **Over-Sampling**: Borderline-SMOTE
- **Hybrid-Sampling**: SMOTEENN

### 5. Model Construction and Evaluation

Models are evaluated using multiple methods, with a custom threshold optimization function to maximize F1-score:

- **Logistic Regression**

  - With original dataset
  - With Tomek-Links dataset
  - With Borderline-SMOTE dataset
  - With SMOTEENN dataset

- **XGBoost**

  - With original dataset
  - With Tomek-Links dataset
  - With Borderline-SMOTE dataset
  - With SMOTEENN dataset

- **Random Forest**
  - With original dataset
  - With Tomek-Links dataset
  - With Borderline-SMOTE dataset
  - With SMOTEENN dataset

### 6. Model Comparison

- Performance metrics across different models and sampling techniques
- Analysis of results and recommendations

## Dependencies

Major libraries used in this project:

- numpy, pandas: Data manipulation
- matplotlib, seaborn: Data visualization
- scikit-learn: Machine learning algorithms and evaluation
- xgboost: Gradient boosting implementation
- imbalanced-learn: Tools for imbalanced classification problems
- scorecardpy: Credit scorecard modeling

## License

[MIT License](LICENSE)

## Acknowledgments

- [Lending Club](https://www.lendingclub.com/) for providing the original data
- [Kaggle](https://www.kaggle.com/datasets/beatafaron/loan-credit-risk-and-population-stability) dataset contributor
