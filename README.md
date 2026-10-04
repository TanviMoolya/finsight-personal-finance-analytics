* FinSight: Personal Expense & Cash Flow Analytics *
FinSight is a personal finance analytics project built to understand everyday money leaks. By breaking down 5 years of personal banking logs, the project tracks where money actually goes each month and measures the real gap between income and expenses.

Project Overview:
Data: 1,500 transaction logs across 60 calendar months (January 2020 – December 2024).
Tools: Python, Pandas, Matplotlib, Google Colab.
Goal: Spot overspending patterns and calculate net monthly savings.

What the Numbers Revealed
Spending Outpaced Earnings: Over 5 years, expenses reached $1.22M across 1,222 transactions, while income totaled only $734K across 278 credits.

The Big 3 Budget Drains: Over 40% of all outgoing cash went to just three buckets:
Travel: $169,497 (13.8%)
Rent: $162,075 (13.2%)
Food & Drink: $159,493 (13.0%)

Consistent Deficit Months: Out of 60 months analyzed, 48 months had negative net cash flow (expenses exceeded income), highlighting recurring monthly overruns rather than isolated one-off splurges.

Analysis & Workflow
Sanity Checks & Cleaning: Verified the data had zero null values and no duplicates, then converted raw date strings to Pandas datetime64.
Feature Extraction: Pulled out year, month, day, and weekday names to track seasonal trends and recurring monthly spikes.
Cash Flow Breakdown: Separated credits (income) from debits (expenses) and grouped outgoing spend across 10 categories.
Net Savings Calculation: Aggregated totals by month and used .unstack(fill_value=0) to line up monthly income against monthly expenses without missing-value errors.
Visual Reporting: Created bar charts, category distribution pies, and a multi-year monthly trend line to make spending habits instantly clear.

Files in this Repository:
Finsight.ipynb – Jupyter notebook containing the full exploratory analysis, aggregations, and charts.
Personal_Finance_Dataset.csv – Raw transactional dataset.
