# Retail Returns Analysis (Order-Level)

## Overview
This project analyzes return behavior in a retail dataset with the goal of
calculating an accurate return rate and identifying categories and products
associated with higher return risk. The analysis emphasizes methodological
consistency, particularly around granularity and KPI definition.

## Dataset
- ~5,000 unique orders
- ~10,000 order-line records
- Multiple product categories per order
- Separate returns and shipping cost datasets

## Methodology
- Returns were analyzed at the **order level**, as a single order may contain
  multiple products and even one returned item results in a returned order.
- An **order-level return flag** was created to ensure correct granularity.
- Category and product analyses were conducted by counting **unique orders**
  rather than order lines.

## Key Findings
- **Overall order-level return rate:** 5.91%
- **Category-level insights:**
  - Office Supplies: 12.64% return rate
  - Technology: 10.10%
  - Furniture: 9.69%
- Returned orders often contain multiple categories, leading to higher
  category-level return rates relative to the overall average.
- Most products have low order frequency (median of 5 orders).
- Several **mid-volume products (15–20 orders)** exhibit disproportionately
  high return rates (>15–20%), making them candidates for further investigation.

## Shipping Cost Context
Shipping cost data was available only at the state level and lacked order-level
identifiers. As a result, shipping variables were not used directly in return
rate calculations. However, higher return rates observed in bulky and furniture
products suggest that logistics-related factors may influence returns and could
be explored further with more granular shipping data.

## Tools
- Python (pandas, numpy)
- Jupyter Notebook / Google Colab

## Takeaway
While the overall return rate is moderate, return behavior varies significantly
by category and product. Focusing on high-risk categories and mid-volume,
high-return products presents an opportunity to reduce returns and improve
operational efficiency.
