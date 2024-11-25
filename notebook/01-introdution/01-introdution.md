# 01 - Introduction to Pandas

## Overview

Pandas is one of the most popular libraries in Python for data manipulation and analysis. It simplifies the process of working with structured data, such as spreadsheets, databases, or even simple lists of information. By offering powerful tools like **Series** and **DataFrame**, Pandas makes it easy to load, clean, and transform data.

Whether you're working on a simple analysis task or a complex data pipeline, Pandas is a go-to tool for Python developers.

---

## Key Features of Pandas

Here are some reasons why Pandas is widely used:

1.  **Fast and efficient**:
    *   Pandas is optimized for performance, making operations on data fast and memory-efficient.
2.  **Versatile DataFrame**:
    *   The DataFrame object allows you to work with structured data in rows and columns, similar to an Excel spreadsheet or SQL table.
3.  **Handling Missing Data**:
    *   Missing data can be tricky to manage, but Pandas provides tools like `.fillna()` and `.dropna()` to handle missing values easily.
4.  **Rich Functionality**:
    *   Tools for reshaping, slicing, grouping, merging, and aggregating data.
5.  **Visualization Support**:
    *   Seamlessly integrates with Matplotlib for quick visualizations.
6.  **Interoperability**:
    *   Works well with other libraries like NumPy, Matplotlib, and Scikit-learn.

---

## Getting Started with Pandas

### 1\. Installing Pandas

If you haven’t installed Pandas, you can do so using pip:

```
pip install pandas
```

### 2\. Importing the Library

After installation, import Pandas into your Python script or notebook:

```python
import pandas as pd
```

### 3\. Pandas Data Structures

Pandas provides two primary data structures:

#### **Series**:

*   A one-dimensional labeled array.
*   Can store any type of data (integers, floats, strings, etc.).
*   Ideal for handling single-column data.

```python
import pandas as pd

# Creating a Series
data = pd.Series([10, 20, 30, 40], index=['a', 'b', 'c', 'd'])
print("Series:\n", data)
```

**Output**:

```
a    10
b    20
c    30
d    40
dtype: int64
```

Key features of a Series:

*   Labeled indices: Each data point is assigned an index (like a row label).
*   Indexing support: Access elements using their labels or positions.

#### **DataFrame**:

*   A two-dimensional labeled data structure (rows and columns).
*   Similar to an Excel sheet or SQL table.
*   Each column in a DataFrame is a Series.

```python
import pandas as pd

# Creating a DataFrame
data = {
    "Name": ["Alice", "Bob", "Charlie"],
    "Age": [25, 30, 35],
    "City": ["New York", "Los Angeles", "Chicago"]
}

df = pd.DataFrame(data)
print("DataFrame:\n", df)
```

**Output**:

```
      Name  Age         City
0    Alice   25     New York
1      Bob   30  Los Angeles
2  Charlie   35      Chicago
```

Key features of a DataFrame:

*   Rows and columns are both labeled.
*   Supports complex operations like filtering, sorting, grouping, and merging.

---

## Why Use Pandas?

Pandas makes working with data more intuitive and efficient. Here’s how:

1.  **Ease of Use**:
    *   With Pandas, complex data transformations that would take dozens of lines of code in plain Python can be done in just one or two lines.
2.  **Real-World Applications**:
    *   Common tasks like handling missing data, merging datasets, or calculating statistics are easy with Pandas.
3.  **Scalability**:
    *   Handles large datasets effectively, making it suitable for real-world projects.
4.  **Integration**:
    *   Easily integrates with libraries for data visualization (Matplotlib, Seaborn) and machine learning (Scikit-learn).

---

## Common Use Cases for Pandas

1.  **Data Cleaning**:
    *   Fix or remove missing and inconsistent data.
2.  **Data Transformation**:
    *   Normalize, group, or pivot data to a usable format.
3.  **Exploratory Data Analysis (EDA)**:
    *   Summarize datasets to uncover patterns and insights.
4.  **Data Storage**:
    *   Read and write data from/to various file formats like CSV, Excel, SQL, JSON, and more.

---

## Exercises

To solidify your understanding, try these exercises:

### Exercise 1:

Create a Pandas Series that represents the population of five cities. Use custom labels to name the cities.

**Example**:

```
City A: 1,000,000
City B: 500,000
City C: 2,000,000
City D: 750,000
City E: 1,250,000
```

### Exercise 2:

Create a Pandas DataFrame representing a list of products with the following columns:

*   Product Name
*   Price
*   Stock Availability  
    Add at least three rows of data.