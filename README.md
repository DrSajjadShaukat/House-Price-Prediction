# California Housing Price Prediction

A learning project using multiple linear regression to predict median house values for California census block groups. Includes a separate notebook for practising SQL with the same dataset.

## Dataset

The California Housing dataset is loaded using scikit-learn.

- Source: 1990 U.S. Census
- Records: 20,640 census block groups
- Input features: 8
- Target: median house value, measured in units of $100,000

Each row represents an area, not an individual house.

## Repository Files

| Notebook | Purpose |
|---|---|
| House_Price_Prediction.ipynb | Data exploration, visualizations, linear regression, and evaluation |
| California_Housing_SQL_Practice.ipynb | SQLite setup and SQL exploration exercises |

## Regression Workflow

1. Load and inspect the dataset.
2. Explore distributions and correlations.
3. Separate input features and target.
4. Split data into 80% training and 20% testing.
5. Train a multiple linear regression model.
6. Evaluate using MAE, MSE, RMSE, and R².

The split uses random_state=42 for reproducibility.

## SQL Practice

The SQL notebook imports the dataset into a local SQLite database and demonstrates:

- SELECT and LIMIT
- WHERE and AND
- ORDER BY with ASC and DESC
- COUNT and AVG
- IS NULL
- GROUP BY
- Column aliases using AS
- Reading query results into pandas

These exercises explore the data separately; their summary results are not additional model features.

## Tools

Python, pandas, NumPy, Matplotlib, Seaborn, scikit-learn, and SQLite.

## How to Run

Open either notebook in Google Colab, or use a local Jupyter environment.

For local use, install the required packages:

    pip install pandas numpy matplotlib seaborn scikit-learn notebook

Run the notebook cells from top to bottom. Internet access is required for the initial dataset download.

Python includes sqlite3. The SQL notebook creates its database when run; rerunning its import cell replaces the housing table.

## Evaluation

The regression notebook reports test-set MAE, MSE, RMSE, and R².

MAE and RMSE can be converted into dollars by multiplying by 100,000. R² is a regression score, not classification accuracy.

## Limitations

- Historical data does not represent current housing prices.
- Predictions concern area-level median values.
- Recorded target values have an upper cap.
- Linear regression may miss nonlinear relationships.
- Correlation alone does not establish causation or feature importance.
- A random train/test split does not establish performance in entirely new geographic regions.

## Author

Dr. Sajjad Shaukat Jamal
