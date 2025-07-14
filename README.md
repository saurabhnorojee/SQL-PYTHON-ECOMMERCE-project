# 🛒 SQL-Python E-Commerce Project

This is a data analysis project combining SQL and Python to simulate and analyze e-commerce data.  
It demonstrates my skills in database design, querying, and data visualization using real-world concepts.

---

## 👨‍💻 About Me

I’m *Saurabh Norojee, a final-year Electrical Engineering student from **MANIT Bhopal*, passionate about data analytics, software development, and solving business problems using data.

---

## 📊 Project Summary

- Built an e-commerce relational database using SQL
- Queried insights like:
  - Best-selling products
  - Revenue trends
  - Top customers
- Visualized the output using *Python (Pandas, Matplotlib)*

---

## 🧰 Tech Stack

- *Python*
- *MySQL / SQLite*
- *Pandas*
- *Matplotlib / Seaborn*
- *Jupyter Notebook*

---

## 📈 Sample Insights
Calculate the number of orders per month in 2018.

query = """ select monthname(order_purchase_timestamp) months, count(order_id) order_count
from orders where year(order_purchase_timestamp) = 2018
group by months
"""

cur.execute(query)

data = cur.fetchall()
df = pd.DataFrame(data, columns = ["months", "order_count"])
o = ["January", "February","March","April","May","June","July","August","September","October"]

ax = sns.barplot(x = df["months"],y =  df["order_count"], data = df, order = o, color = "red")
plt.xticks(rotation = 45)
ax.bar_label(ax.containers[0])
plt.title("Count of Orders by Months is 2018")

plt.show()

<img width="580" height="505" alt="download" src="https://github.com/user-attachments/assets/8451d483-a620-41c8-9148-b6c7c683e219" />

## 💼 What I Learned

-  Writing optimized SQL queries for real business data
-  Data transformation using Pandas
-  Visualizing insights with charts (bar, pie, line)
-  Structuring data in relational models (normalization, keys)

> 🔍 This project showcases practical data analytics using SQL and Python.
> It simulates a real e-commerce scenario to derive business insights like revenue trends, product performance, and customer loyalty.
