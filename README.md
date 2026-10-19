# 50 Startups Profit Prediction (Multiple Linear Regression)

A beginner-friendly machine learning project that predicts a startup's **Profit** from its spending using **Multiple Linear Regression** in Python.

## Dataset

- **Source:** [50 Startups dataset on Kaggle](https://www.kaggle.com/)
- **File:** `50_Startups.csv`
- **Rows:** 50 startups

| Column | Type | Description |
|---|---|---|
| R&D Spend | Numeric | Money spent on research and development |
| Administration | Numeric | Money spent on administration |
| Marketing Spend | Numeric | Money spent on marketing |
| State | Categorical | State where the startup is located |
| Profit | Numeric | **Target:** profit of the startup |

## Project Workflow

1. Load the data with Pandas
2. Explore it with `info()`, `isnull().sum()` and `describe()`
3. Visualize correlations with a Seaborn heatmap
4. Encode the categorical column (`State`) with `pd.get_dummies`
5. Split data into train (80%) and test (20%)
6. Train a `LinearRegression` model
7. Evaluate with R² and RMSE
8. Inspect the coefficients

## Key Observations from the Correlation Heatmap

- **R&D Spend** has a very strong positive correlation with Profit (about 0.97).
- **Marketing Spend** has a moderate to strong correlation with Profit (about 0.75).
- **Administration** has a weak correlation with Profit (about 0.2).
- R&D Spend and Marketing Spend are correlated with each other (about 0.72), so mild multicollinearity is possible.

## Results

| Metric | Value |
|---|---|
| R² (train) | _add your value_ |
| R² (test) | _add your value_ |
| RMSE (test) | _add your value_ |
## Results

| Metric | Value |
|--------|-------|
| R² Score | 0.8987 |
| MSE | 82,010,363 |
| RMSE | ~9,056 |

| Feature | Coefficient |
|---------|-------------|
| R&D Spend | 0.8056 |
| Administration | -0.0688 |
| Marketing Spend | 0.0299 |
| State_Florida | 938.79 |
| State_New York | 6.99 |

Intercept: 54028.04

### Key Takeaway
The model explains about 90% of the variance in profit on the test set. R&D Spend has the strongest positive effect on profit, while Administration, Marketing Spend and State have a much smaller impact.

## Technologies Used

- Python 3
- Pandas
- NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Statsmodels (VIF)
- Jupyter Notebook (VS Code)

## How to Run

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>

# 2. Install the requirements
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels jupyter

# 3. Open the notebook
jupyter notebook "multi linear regrrasion.ipynb"
```

## Project Structure

```
.
├── 50_Startups.csv
├── multi linear regrrasion.ipynb
└── README.md
```

## What I Learned

- How multiple linear regression works (`y = b0 + b1*x1 + b2*x2 + ...`)
- How to read a correlation heatmap and spot multicollinearity
- How to encode categorical data and split data for training and testing
- How to evaluate a regression model with R² and RMSE

## Author

**Shazia Batool**
AI student at COMSATS University
