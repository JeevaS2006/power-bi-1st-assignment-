# Power BI E-commerce Sales Data Preparation and Modeling

## 📌 Project Overview

This project focuses on data preparation, transformation, cleansing, aggregation, and relationship modeling using Microsoft Power BI and Power Query Editor.

As part of this assignment, I worked with multiple e-commerce datasets containing order information, product details, and sales targets. The main objective was to transform raw data into a clean, consistent, and structured format and establish relationships between tables to support meaningful business analysis.

This project demonstrates my understanding of data preparation, Power Query transformations, data integration, and data modeling as part of my journey as an **Aspiring Data Analyst**.

## 🎯 Project Objectives

* Import multiple CSV datasets into Power BI.
* Clean and transform raw data using Power Query Editor.
* Handle missing values, inconsistent data, and duplicate records.
* Apply appropriate data types and text formatting.
* Create calculated columns using custom and conditional logic.
* Merge related datasets using appropriate join operations.
* Group and aggregate data to generate meaningful summaries.
* Establish relationships between tables using common fields.
* Build a structured data model for future business analysis.

## 📂 Datasets Used

This project uses three datasets:

### 1. List of Orders

Contains order-level information about customers, locations, sales, and profitability.

**Key Columns:**

* Order ID
* Order Date
* Customer Name
* City
* State
* Category
* Amount
* Profit

### 2. Order Details

Contains detailed information about product categories, sub-categories, quantities, sales amounts, and profits.

**Key Columns:**

* Order ID
* Category
* Sub-Category
* Quantity
* Amount
* Profit

### 3. Sales Target

Contains monthly sales targets for different product categories.

**Key Columns:**

* Category
* Month of Order Date
* Target

## 🛠️ Tools and Technologies

* **Microsoft Power BI Desktop** – Data modeling and dataset integration.
* **Power Query Editor** – Data cleaning and transformation.
* **CSV Files** – Source datasets.
* **Power Query M** – Data transformation logic and custom column creation.
* **GitHub** – Project documentation and portfolio management.

## 🔄 Project Workflow

### 1. Data Import

* Imported List of Orders, Order Details, and Sales Target CSV files into Power BI.
* Opened Power Query Editor using the Transform Data option.
* Reviewed the structure and columns of each dataset.

### 2. Data Transformation

* Restricted the List of Orders dataset to the first 500 rows.
* Changed the Order Date column to the Date data type.
* Converted Amount and Target columns to Fixed Decimal Number where appropriate.
* Formatted Customer Name using Proper Case to maintain consistent capitalization.

### 3. Custom Column Creation

**Location**

Combined the City and State columns into a new column named `Location`.

Format:
`City, State`

**Profit Margin**

Created a custom column to calculate profit margin as a percentage of sales.

Formula:
`Profit Margin = (Profit / Amount) × 100`

This calculation helps evaluate profitability relative to sales.

*Note: When displaying the result as a percentage in Power BI, the underlying calculation and formatting must be consistent. If the calculated value is `Profit / Amount`, apply percentage formatting rather than multiplying by 100 again.*

**Profit Status**

Created a conditional column named `Profit Status` using the following business rules:

| Condition  | Profit Status |
| ---------- | ------------- |
| Profit < 0 | Loss          |
| Profit = 0 | Break-Even    |
| Profit > 0 | Profit        |

This classification helps identify profitable, loss-making, and break-even orders.

### 4. Data Merging

* Merged List of Orders and Order Details using the common `Order ID` column.
* Named the merged output table `Orders Data`.
* Used the matching Order ID values to combine relevant order-level and order-detail information.

This integration helps bring related information together for further analysis.

### 5. Missing Values and Duplicate Handling

* Inspected all three datasets for missing and null values.
* Evaluated missing values based on the importance of each column.
* Retained null values when the original information could not be reliably recovered.
* Replaced missing values only when an appropriate replacement could be justified.
* Identified duplicate records and considered their impact before removing them.
* Avoided deleting valid records or replacing missing numerical values with zero without justification.

These steps help maintain data quality and reliability.

### 6. Sorting and Filtering

* Sorted the Orders Data table by Order Date in descending order.
* Applied state-level filters, including Tamil Nadu, to examine location-specific records.

Sorting and filtering help organize records and support focused analysis.

### 7. Grouping and Aggregation

**Order Details Analysis**

Created a duplicate of the Order Details query and performed the following aggregations:

* Count of Order ID.
* Average Profit by Category.
* Total Amount by Sub-Category.

These aggregations help summarize order activity, category-level profitability, and sub-category sales performance.

**Sales Target Analysis**

Created a duplicate of the Sales Target query and aggregated the total Target by Month of Order Date.

This provides a monthly summary of sales targets.

### 8. Data Modeling

Established relationships between the datasets using common fields.

**Relationship 1: List of Orders and Order Details**

* Common Column: `Order ID`
* Purpose: Connect order-level information with detailed order records.

**Relationship 2: Order Details and Sales Target**

* Common Column: `Category`
* Purpose: Connect product category information with corresponding sales targets.

Used Manage Relationships in Power BI to verify that the relationships were active and correctly defined.

*Note: The relationship cardinality should be determined from the actual data. If a key occurs multiple times in both tables, validate the model carefully to avoid ambiguous filtering and incorrect aggregations.*

## 📊 Key Learning Outcomes

Through this project, I developed practical knowledge of:

* Importing and transforming multiple datasets in Power BI.
* Using Power Query Editor for data cleansing and preparation.
* Applying data types and text formatting.
* Creating custom and conditional columns.
* Merging tables using common identifiers.
* Handling missing values and duplicate records.
* Grouping and aggregating data for business analysis.
* Establishing relationships between tables.
* Understanding how data quality affects analytical accuracy.
* Preparing structured datasets for further reporting and visualization.

## 📁 Project Files

The repository is organized to include the following files:

```text
PowerBI-Ecommerce-Data-Modeling/
│
├── README.md
│
├── Dataset/
│   ├── List of Orders.csv
│   ├── Order Details.csv
│   └── Sales target.csv
│
├── PowerBI/
│   └── E-commerce_Data_Modeling.pbix
│
└── Documentation/
    └── PowerBI_Assignment_Report.pdf
```

*Note: This is the suggested folder structure. Update the file names and folders to match the actual contents of your repository.*

## 🚀 Conclusion

This project provided hands-on experience in preparing and modeling e-commerce sales data using Microsoft Power BI. By applying data cleaning, transformation, merging, aggregation, and relationship modeling techniques, I developed a structured dataset suitable for further business analysis.

The project strengthened my understanding of data preparation workflows and the importance of maintaining data consistency, accuracy, and meaningful relationships between datasets.

As an **Aspiring Data Analyst**, I am continuously developing my skills in data analysis, visualization, and business intelligence through practical projects.

## 👨‍💻 Author

**Jeeva S**

Aspiring Data Analyst

**Areas of Interest:**

* Data Analysis
* Microsoft Excel
* Power BI
* SQL
* Python
* Data Visualization
* Business Intelligence

---

⭐ If you find this project useful, feel free to explore the repository.
