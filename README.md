Home_Sales
# 🏠✨ **Spark SQL Performance Analysis** ✨🏠

## 🚩 **Overview:**
This assignment demonstrates how to use **Apache Spark SQL** to efficiently handle big data, focusing on:
- Loading and querying data.
- Creating temporary views.
- Caching data for improved performance.
- Partitioning data and saving in Parquet format.
- Performance benchmarking.

---

## 🔧 **Technologies Used:**

- ✅ **Apache Spark (v3.5.5)**
- ✅ **PySpark (Spark SQL)**
- ✅ **Google Colab**
- ✅ **Parquet Data Format**

---

## 📌 **Dataset Used:**

- **home_sales_revised.csv**
- Contains home sales data with attributes such as date built, bedrooms, bathrooms, floors, square footage, view rating, and price.

---

## 📚 **Steps Completed:**

### 1️⃣ **Setup & Data Loading**
- Apache Spark session initialized.
- Loaded CSV data into PySpark DataFrame (`home_sales_df`).

### 2️⃣ **Temporary View Creation**
- Created Spark temporary view (`home_sales`) for SQL queries.

### 3️⃣ **Queries Performed:**
- **Average price per year** for 4-bedroom homes.
- **Average price per built-year** for homes with 3 bedrooms and 3 bathrooms.
- **Average price per built-year** for homes with 3 bedrooms, 3 bathrooms, 2 floors, and ≥2000 sqft.
- **Average price per view rating** (≥ $350,000 average price).

### 4️⃣ **Data Optimization Techniques:**
- **Caching** temporary views.
- **Partitioning** data by `date_built` and saving as Parquet.

---

## 🚀 **Performance Benchmark Results:**

| Method             | Runtime (seconds) ⏱️ |
|--------------------|----------------------|
| 🔴 **Uncached**    | `0.742`              |
| 🟢 **Cached**      | `0.546` (**Fastest**) |
| 🔵 **Partitioned** | `0.676`              |

### 📊 **Performance Insights:**
- **Caching** significantly reduces runtime due to memory optimization.
- **Partitioning** improves performance by efficiently accessing relevant data partitions, though slightly slower than fully cached data.
- **Uncached data** shows slowest performance due to repeated disk I/O operations.

---

## 🎯 **Conclusions & Best Practices:**
- 🟢 **Caching**: Best for repeated queries on the same dataset.
- 🔵 **Partitioning**: Ideal for improving efficiency on larger datasets stored on disk.
- 🛠️ Combining caching and partitioning can provide optimal query performance.

---

## ✨ **Final Thoughts:**
This exercise highlights how powerful Apache Spark SQL optimization techniques like caching and partitioning can drastically improve big-data processing performance. By strategically applying these methods, you can achieve efficient data analysis at scale.

🌟 **Happy Sparking!** 🌟

