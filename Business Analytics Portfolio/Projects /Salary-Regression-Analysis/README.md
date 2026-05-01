# Salary Prediction — Linear Regression

Predicting employee salary from years of experience using simple linear regression.

---

## Overview

This project walks through a complete regression pipeline on a real-world salary dataset. The goal is to model the relationship between years of experience and annual salary, evaluate how well a linear model captures that relationship, and visualize the results clearly.

## Project Structure

```
salary-regression-analysis/
├── README.md
├── requirements.txt
├── data/
│   └── Salary_dataset.csv
├── notebooks/
    └── salary_regression.ipynb

```

## Methodology

| Step | Description |
|---|---|
| EDA | Summary statistics, missing value and duplicate checks |
| Correlation | Pearson correlation matrix + heatmap |
| Preprocessing | Min-Max normalization on both `X` and `y` |
| Split | 80% training / 20% testing (`random_state=42`) |
| Model | Scikit-learn `LinearRegression` |
| Evaluation | R², MAE, RMSE (reported in original dollar scale) |

## Results

The model achieves strong performance on this dataset, reflecting the high linear correlation between experience and salary. Both training and test R² scores are close, indicating no significant overfitting.

## Visualizations

Three plots are produced and saved to `visuals/`:

- **Regression Fit** — scatter plot of all data points with the fitted regression line
- **Train/Test Split** — the same plot with training and test points colored separately
- **Actual vs. Predicted** — parity plot for test set predictions against ground truth

## Tech Stack

- Python 3.11
- pandas, NumPy
- scikit-learn
- matplotlib, seaborn

## How to Run

```bash
# 1. Clone the repo
git clone https://github.com/yourusername/salary-regression-analysis.git
cd salary-regression-analysis

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch the notebook
jupyter notebook notebooks/salary_regression.ipynb
```

## Dataset

`Salary_dataset.csv` — a simple two-column dataset containing `YearsExperience` and `Salary` for a set of employees. Source: publicly available regression benchmark dataset.
