# 02 - Loading and Exploring Data

## Overview

In real-world applications, data often comes from external sources like CSV files, Excel spreadsheets, databases, or APIs. Pandas provides powerful functions to load, inspect, and understand these datasets.

---

## Loading Data into Pandas

Pandas supports a variety of file formats. Here are some common methods:

**CSV Files**:

*   Use `pd.read_csv()` to load data from a CSV file.
*   Example:

```python
import pandas as pd 
# Load CSV file
df = pd.read_csv("data.csv")
print(df.head()) 
# Display the first 5 rows
```

**Excel Files**:

*   Use `pd.read_excel()` to load data from Excel spreadsheets.
*   Example:

```python
# Load Excel file
df = pd.read_excel("data.xlsx", sheet_name="Sheet1")
print(df.info())  # Display summary information
```

**JSON Files**:

*   Use `pd.read_json()` to load data from JSON files.
*   Example:

```python
# Load JSON file
df = pd.read_json("data.json")
print(df.describe())  
# Display statistical summary
```

**SQL Databases**:

*   Use `pd.read_sql_query()` to load data from SQL queries (requires a database connection).

---

## Exploring Data

After loading the data, it’s crucial to inspect its structure and understand its content. Here are some useful methods:

**Basic Information**:

*   `df.info()` – Displays metadata, such as data types and memory usage.
*   `df.shape` – Returns the number of rows and columns.
*   Example:

```python
print(df.info())
print("Shape:", df.shape)
```

**Preview the Data**:

*   `df.head()` – Displays the first 5 rows (useful for previewing data).
*   `df.tail()` – Displays the last 5 rows.
*   Example:

```python
print(df.head())
print(df.tail())
```

**Column and Index Information**:

*   `df.columns` – Lists all column names.
*   `df.index` – Displays row index information.
*   Example:

```python
print("Columns:", df.columns)
print("Index:", df.index)
```

**Summary Statistics**:

*   `df.describe()` – Provides a statistical summary (mean, std, min, etc.) for numeric columns.
*   Example:

```python
print(df.describe())
```

---

## Exercises

### Exercise 1:

Load a CSV file named `sales.csv` containing the following data:

| Product | Units Sold | Revenue |
| --- | --- | --- |
| Laptop | 5 | 6000 |
| Smartphone | 10 | 8000 |
| Headphones | 15 | 1500 |

1.  Use Pandas to load this file.
2.  Display the first 2 rows using `.head()`.
3.  Print the shape of the dataset.

### Exercise 2:

Create a DataFrame manually with the following data:

| Name | Age | Department |
| --- | --- | --- |
| Alice | 25 | HR |
| Bob | 30 | IT |
| Charlie | 35 | Marketing |

1.  Display the column names and index information.
2.  Print the summary statistics using `.describe()`.