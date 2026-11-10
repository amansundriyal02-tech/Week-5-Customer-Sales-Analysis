# Week 5: Customer Sales Analysis

## Project overview
Customer and sales analysis using Pandas: cleaning, filtering, string transformations, datetime extraction, groupby aggregations, merging, pivot tables and visualizations.

## Files
- `customer_analysis.ipynb` — complete executable notebook
- `sales_data.csv` — supplied sales dataset (cleaned)
- `customer_data.csv` — customer profile lookup derived from sales records
- `customer_churn.csv` — supplied customer churn dataset (cleaned)
- `outputs/` — summaries, pivot table, charts and written report
- `requirements.txt` — dependencies

## Run
```bash
python -m pip install -r requirements.txt
jupyter notebook customer_analysis.ipynb
```

## Important data note
The sales IDs (`CUST001` format) and churn IDs (`C00001` format) are not a verified common key. The notebook does not falsely join these records. It merges sales transactions with a customer profile lookup derived from the sales file. Churn is analyzed separately as a retention-risk proxy.

The sales data has no order/basket ID, so cross-selling/product-pair analysis cannot be reliably calculated. The churn data has no transaction dates, so repeat-purchase retention cannot be calculated.
