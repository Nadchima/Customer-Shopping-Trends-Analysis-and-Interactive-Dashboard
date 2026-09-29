# Customer Shopping Trends Analysis and Interactive Dashboard

An exploratory customer-shopping analysis in Python with visual summaries and an interactive Jupyter widget for filtering sales by season, category, location, age range, gender, and chart type.

## Project objective

- Analyze consumer behavior and purchasing trends in the dataset.
- Identify demographic and behavioral factors associated with sales.
- Create an interactive interface with `ipywidgets` for user-selected analysis.

## Tools and data

- Python, pandas, NumPy, Matplotlib, Seaborn, and ipywidgets
- Google Colab/Jupyter Notebook
- [Customer Shopping Behavior Dataset on Kaggle](https://www.kaggle.com/datasets/ayeshasiddiqa123/customer-shopping-behavior-dataset)

The included dataset contains 3,900 transactions and 18 fields covering customer demographics, product details, purchase amount, location, season, subscription status, shipping, discounts, payment method, and purchase frequency.

| Data-quality check | Result |
|---|---:|
| Rows | 3,900 |
| Columns | 18 |
| Missing values | 0 |
| Duplicate rows | 0 |
| Total purchase amount | USD 233,081 |

## Analysis workflow

1. Load the source data and validate its schema.
2. Check missing values and duplicate rows.
3. Profile product, location, season, shipping, and purchase-frequency distributions.
4. Aggregate purchase amount and customer counts.
5. Visualize location, category, season, frequency, subscription, and gender patterns.
6. Explore filtered results through interactive Jupyter widgets.

## Interactive dashboard

The dashboard supports filters for season, product category, customer location, age range, optional gender split, and bar or pie chart display.

<img width="876" height="491" alt="Interactive customer shopping dashboard" src="https://github.com/user-attachments/assets/87cd9c67-09c1-455e-b4b5-818e994142fb" />

## Key findings

### Best-selling categories

Clothing is the primary revenue driver, generating USD 104,264 in sales, followed by Accessories at USD 74,200.

<img width="536" height="222" alt="Sales by product category" src="https://github.com/user-attachments/assets/c29de7b9-233c-4aba-9f6b-ed5ae864767d" />

### Customer profile

The source sample contains more male than female customers. Male spending is therefore higher in raw totals across the product categories, but this should not be interpreted as stronger preference without normalizing for the unequal group sizes.

<img width="526" height="485" alt="Purchases by gender and category" src="https://github.com/user-attachments/assets/6575efd7-913a-4fd2-8727-76e81609378d" />

### Membership opportunity

Subscribers represent 27% of records. The remaining 73% form a large non-subscriber segment that could be explored for loyalty and retention campaigns.

<img width="375" height="179" alt="Subscription status distribution" src="https://github.com/user-attachments/assets/df19f6fa-1d1d-4bc5-a5c9-339badeb8be7" />

## Repository contents

```text
.
├── final_project.py
├── shopping_behavior_updated.csv
├── Customer Shopping Trends Dataset.pdf
└── README.md
```

## Run locally

```bash
pip install pandas numpy matplotlib seaborn ipywidgets kagglehub
jupyter notebook
```

The Python file was exported from Google Colab. For the best widget experience, paste or convert it back into a notebook and enable `ipywidgets` in Jupyter.

## Limitations and next steps

- The data is observational and does not establish causality.
- Normalize gender comparisons because the source sample is imbalanced.
- The dashboard uses purchase amount as sales and does not include product cost or profit.
- Confirm dataset licensing and provenance before redistribution.
- Add cohort, retention, average-order-value, and discount-response analyses.
- Package the interactive analysis as a Streamlit or Plotly Dash application.
