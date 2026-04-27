# 🛒 E-Commerce Business Intelligence — SQL Analytics Project

A data analytics project built on a Brazilian e-commerce dataset. Raw CSV data is ingested into a SQLite database and queried using SQL inside a Jupyter Notebook to answer key business questions, with results visualized using Matplotlib and Seaborn.

---

## 📁 Project Structure

```
ecommerce-analytics/
│
├── ingestion.py                 # Script to load CSVs into SQLite database
├── business_queries.ipynb       # Jupyter Notebook with SQL queries & visualizations
├── requirements.txt             # Python dependencies
└── README.md                    # Project documentation
```

---

## 🗄️ Database Schema

The SQLite database (`ecommerce.db`) contains 7 tables:

| Table         | Rows      | Description                                      |
|---------------|-----------|--------------------------------------------------|
| `customers`   | 99,441    | Customer IDs, cities, states, and zip codes      |
| `geolocation` | 1,000,163 | Lat/lng coordinates mapped to zip code prefixes  |
| `orders`      | 99,441    | Order lifecycle timestamps and statuses          |
| `order_items` | 112,650   | Products, sellers, prices, and freight per order |
| `payments`    | 103,886   | Payment type, installments, and values           |
| `products`    | 32,951    | Product categories, dimensions, and weights      |
| `sellers`     | 3,095     | Seller IDs, cities, and states                   |

---

## 📊 Business Questions Answered

### Basic Queries
1. List all unique cities where customers are located
2. Count the number of orders placed in 2017
3. Find the total sales per product category
4. Calculate the percentage of orders paid in installments
5. Count the number of customers from each state

### Intermediate Queries
6. Calculate the number of orders per month in 2018
7. Find the average number of products per order, grouped by customer city
8. Calculate the percentage of total revenue contributed by each product category
9. Identify the correlation between product weight/dimensions and freight value
10. Identify the top 3 sellers by total revenue (with visualization)

### Advanced Queries
11. Calculate the moving average of order values per customer over their order history
12. Identify the cumulative sales per month for each year
13. Calculate the year-over-year growth rate of total sales
14. Retain the top 3 customers by total payment amount for each year (with visualization)
15. Calculate the retention rate of customers, defined as the percentage of customers who make another purchase within 6 months of their first purchase.

---

## 🚀 Getting Started

### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

### 2. Download the Dataset

Download the dataset from [Kaggle — Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) and place the CSV files in the same folder as `ingestion.py`.

### 3. Run the Ingestion Script

```bash
python ingestion.py
```

This will read the CSV files and load them into `ecommerce.db`.

### 4. Open the Notebook

```bash
jupyter notebook business_queries.ipynb
```

---

## 🧰 Tech Stack

- **Python 3.11**
- **SQLite** — lightweight local database
- **Pandas** — data manipulation and SQL query execution
- **Matplotlib & Seaborn** — data visualization
- **NumPy** — numerical operations
- **Jupyter Notebook** — interactive analysis environment

---

## 📦 requirements.txt

```
pandas
matplotlib
seaborn
numpy
jupyter
```

---

## 📌 Dataset Source

[Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) — available on Kaggle under a Creative Commons license.

---

