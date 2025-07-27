(SQLite + Python Data Summary)

🧮 Get Basic Sales Summary using SQLite and Python

This project is a part of Task 7 from my Data Analyst Internship at Elevate Labs. The objective is to use SQL inside Python to pull basic sales info (like total quantity and total revenue), and visualize the results using a simple bar chart.


---

⚙️ Tools Used

Python (sqlite3, pandas, matplotlib)

SQLite (built into Python — no extra installation needed)

Jupyter Notebook or .py script file



---

📂 Dataset

Create a small SQLite database sales_data.db containing one table sales, with columns like:

product

quantity

price



---

📌 Steps (Mini Guide)

1. Connect to the Database

import sqlite3  
conn = sqlite3.connect("sales_data.db")


2. Run Basic SQL Query

SELECT product, SUM(quantity) AS total_qty, SUM(quantity * price) AS revenue  
FROM sales  
GROUP BY product;


3. Import Data into Pandas

import pandas as pd  
df = pd.read_sql_query(query, conn)


4. Print Results

print(df)


5. Plot Bar Chart (Revenue by Product)

import matplotlib.pyplot as plt  
df.plot(kind='bar', x='product', y='revenue')  
plt.savefig("sales_chart.png")




---

🎯 Outcome of Task

By completing this task, you will:

Learn to write and run SQL queries

Import SQL data directly into Python

Generate simple data summaries

Plot your first sales bar chart using matplotlib



---

📁 Files Included

sales_data.db – SQLite database

task7_summary.py / task7_notebook.ipynb – Python code file

sales_chart.png – Bar chart output

README.md – This file



---

❓ Interview Questions (Practice)

How did you connect Python to a database?

What SQL query did you run?

What does GROUP BY do?

How did you calculate revenue?

How did you visualize the result?

What does read_sql_query() do in your code?

Could you run this query in DB Browser for SQLite?
