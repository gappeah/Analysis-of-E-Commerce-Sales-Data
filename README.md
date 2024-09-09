# E-Commerce Sales Data Analysis

## Project Overview

This project focuses on analyzing sales data from an e-commerce platform. The goal is to gain insights into sales patterns, identify trends, and provide actionable recommendations based on the data. The analysis includes examining product categories, sales performance, and customer behavior.

## Features

- **Data Cleaning**: Handling missing values, correcting data types, and removing outliers.
- **Exploratory Data Analysis (EDA)**: Visualizing key metrics such as sales distribution across categories, time-based trends, and product performance.
- **Descriptive Statistics**: Summary statistics for product categories and their sales performance.
- **Visualizations**: Graphs and plots to communicate findings, including bar charts and sales distributions.
  
## Technologies Used

- **Python**: Programming language used for data manipulation and analysis.
- **Pandas**: For data wrangling and manipulation.
- **Matplotlib & Seaborn**: For generating visualizations.
- **Jupyter Notebook**: For interactive data analysis.

## Dataset Preview

The dataset consists of various fields such as `product_category`, `sales`, and `order_date`. Below is a preview of the first few rows of the dataset:

| order_id | product_category | sales | order_date  |
|----------|------------------|-------|-------------|
| 1        | Clothing          | 1200  | 2023-06-01  |
| 2        | Electronics       | 1500  | 2023-06-02  |
| 3        | Home Goods        | 700   | 2023-06-03  |
| 4        | Clothing          | 850   | 2023-06-04  |
| 5        | Electronics       | 1300  | 2023-06-05  |

## Key Findings

1. **Product Categories**:
   - The dataset is grouped by product categories like Clothing, Electronics, and Home Goods.
   - Electronics category exhibits higher variance in sales compared to other categories.

2. **Sales Performance**:
   - Mean and median sales values were calculated per category.
   - The analysis revealed that Clothing and Electronics have similar sales averages, but Electronics sales exhibit more variability.

![output_2](https://github.com/user-attachments/assets/89f5834a-6ed1-4fca-afcb-1d6b4f4f20b5)
![output_1](https://github.com/user-attachments/assets/20b61fd7-06c7-44dc-8574-0d098775964f)
![output](https://github.com/user-attachments/assets/c4a1ed8d-35ab-4e47-9ff2-81c102680f60)

## Code Examples

Here are some code snippets from the project:

### 1. Data Loading and Preview

```python
import pandas as pd

# Load the dataset
sales_data = pd.read_csv('data/ecommerce_sales.csv')

# Preview the first few rows
print(sales_data.head())
```

### 2. Grouping Data by Product Category

```python
# Group by product category and calculate descriptive statistics for sales
category_summary = sales_data.groupby('product_category')['sales'].describe()
print(category_summary)
```

### 3. Visualizing Sales by Product Category

```python
import seaborn as sns
import matplotlib.pyplot as plt

# Plot sales distribution for each product category
plt.figure(figsize=(10, 6))
sns.boxplot(x='product_category', y='sales', data=sales_data)
plt.title('Sales Distribution by Product Category')
plt.show()
```

## Getting Started

### Running in Visual Studio Code

To run the notebook in **Visual Studio Code**, follow these steps:

1. **Install Visual Studio Code**: Download and install VS Code from [here](https://code.visualstudio.com/).

2. **Install Python Extension**: Open VS Code and install the "Python" extension from the extensions marketplace.

3. **Install Jupyter Extension**: You will also need the "Jupyter" extension to open `.ipynb` files.

4. **Clone the Repository**:
   ```bash
   git clone https://github.com/gappeah/Analysis-of-E-Commerce-Sales-Data.git
   ```

5. **Open the Project Folder**: In VS Code, open the folder containing the project files.

6. **Open and Run the Notebook**: Open the `Analysis_of_E-Commerce_Sales_Data.ipynb` file in VS Code and run the cells interactively using the Jupyter environment.

### Running in Google Colab

If you prefer running the notebook in **Google Colab**, follow these steps:

1. **Upload the Notebook to Colab**:
   - Go to [Google Colab](https://colab.research.google.com/).
   - Click on **File** > **Upload Notebook** and select the `Analysis_of_E-Commerce_Sales_Data.ipynb` file from your local machine.

2. **Install Necessary Libraries**: If the notebook requires additional Python libraries that are not pre-installed on Colab, you can install them by running:
   ```python
   !pip install -r requirements.txt
   ```

3. **Run the Notebook**: Once all the dependencies are installed, run the cells by clicking the play icon next to each code block.

## Files

- `Analysis_of_E-Commerce_Sales_Data.ipynb`: The main notebook containing the analysis.
- `customer_data`, `product_data`, `retail_sales_data` : Contains the datasets used for the analysis.
- `README.md`: This file.
