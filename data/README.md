# Data Directory

This directory is intended to store data files used in the credit risk analysis project.

## Lending Club Dataset

The data used in this project comes from the Lending Club Company public database and is available on Kaggle:
[Loan - Credit Risk & Population Stability](https://www.kaggle.com/datasets/beatafaron/loan-credit-risk-and-population-stability?select=loan_2014_18.csv)

### Dataset Files

The dataset is divided into two parts:

1. **loan_2014-2018.csv**: Contains almost 1,800,000 consumer loans issued from 2014 to 2018.
2. **loan_2019-2020.csv**: Separate data to validate if the model has similar characteristics and is still up to date.

Note: I only use `loan_2014-2018.csv`.

### About Lending Club

LendingClub is a US peer-to-peer lending company headquartered in San Francisco, California. It was the first peer-to-peer lender to register its offerings as securities with the Securities and Exchange Commission (SEC) and to offer loan trading on a secondary market. LendingClub is the world's largest peer-to-peer lending platform.

## Data Usage

Due to the large size of the dataset (nearly 1.8 million records), you need to:

1. Download the dataset from Kaggle using the link above
2. Place the CSV files in this directory
3. Follow the instructions in the Jupyter notebook for loading and preprocessing the data

## Data Structure

The dataset contains numerous features related to loan applications, including:

- Loan amount
- Interest rate
- Term length
- Borrower information (income, employment, etc.)
- Loan status (target variable indicating default)
- Credit metrics and risk indicators

## Data Processing

The notebook contains comprehensive steps for:

- Handling missing values
- Feature selection and engineering
- Normalization and scaling
- Dimensionality reduction through PCA
- Class imbalance handling through various sampling techniques

Please refer to the Jupyter notebook in the `notebooks/` directory for detailed processing instructions.
