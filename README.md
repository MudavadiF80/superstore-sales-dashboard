# Superstore Sales Dashboard

An interactive sales analytics dashboard built with **Python, Streamlit, Pandas, and Plotly**. It turns raw Superstore sales data into KPIs, filterable charts, and regional and product insights.

**Live demo:** [superstore-sales-dashboard-mudavadif80.streamlit.app](https://superstore-sales-dashboard-mudavadif80.streamlit.app/)


## Overview

Retail businesses generate large volumes of transaction data, but raw spreadsheets make it hard to spot trends, judge profitability, or compare categories and regions. This dashboard lets users filter the data and see the key performance indicators update in real time.

## Features

### Key Performance Indicators

- **Total Sales:** Total revenue from orders
- **Total Profit:** Overall profit from sales
- **Total Quantity:** Units sold
- **Profit Margin:** Profit as a percentage of sales

### Interactive Filters

Sidebar controls let users narrow the data by:

- Order date range
- Product category
- Sales region
- Customer segment

All KPIs and charts update when filters change. If no records match, the dashboard shows a warning instead of empty charts.

### Visualizations

- **Monthly Sales Trend:** Revenue over time, to spot growth patterns and seasonality
- **Sales by Category:** Revenue comparison across product categories
- **Profit by Sub-Category:** Which sub-categories drive profit and which lose money
- **Sales Distribution by Region:** Share of sales across regions

All charts are interactive, with hover details for each data point.

### Filtered Data Table

A table at the bottom shows the rows behind the current selection, with a count of filtered versus total records.

## Data Preparation

The app uses Pandas to:

- Convert order dates to datetime, coercing invalid values to missing
- Convert sales, profit, and quantity to numeric values
- Drop rows missing essential fields
- Group data by month, category, sub-category, and region
- Apply all filters before calculating metrics and rendering charts

## Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core language |
| Streamlit | Web app and dashboard framework |
| Pandas | Data cleaning, transformation, and aggregation |
| Plotly Express | Interactive charts |

## Project Structure

```text
superstore-sales-dashboard/
├── app.py              # Streamlit application
├── Superstore.csv      # Sales dataset
├── requirements.txt    # Python dependencies
├── .gitignore
└── README.md
```

## Run Locally

### Prerequisites

- Python 3.9 or later

### 1. Clone the repository

```bash
git clone https://github.com/MudavadiF80/superstore-sales-dashboard.git
cd superstore-sales-dashboard
```

### 2. Create and activate a virtual environment (recommended)

```bash
python -m venv venv
```

**Windows:**

```bash
venv\Scripts\activate
```

**macOS/Linux:**

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the app

```bash
streamlit run app.py
```

The app opens at `http://localhost:8502`.

## Deploy on Streamlit Community Cloud

1. Push the repository to GitHub.
2. Go to [share.streamlit.io](https://share.streamlit.io) and sign in with GitHub.
3. Click **Create app**, then **Deploy a public app from GitHub**.
4. Set the repository, branch (`main`), and main file path (`app.py`), then click **Deploy**.

Streamlit installs the packages in `requirements.txt` automatically. Future pushes to `main` redeploy the app.

## Business Questions Explored

1. How do monthly sales change over time?
2. Which product categories generate the most revenue?
3. Which sub-categories contribute most to profit?
4. How does performance differ across regions?
5. How do customer segments and date ranges affect results?

## Skills Demonstrated

- Data cleaning and preprocessing
- Exploratory data analysis
- Business KPI calculation
- Time-series analysis
- Data aggregation and grouping
- Interactive dashboard development
- Data visualization with Plotly
- Building and deploying Python web apps with Streamlit

## Future Improvements

- Period-over-period comparisons and growth metrics
- Year-over-year performance analysis
- Loss-making product and category identification
- Downloadable filtered reports
- Database integration for larger datasets

## Author

**Francis Mudavadi**, [MudavadiF80](https://github.com/MudavadiF80)
Data Analytics | Python | Business Intelligence | Dashboard Development
