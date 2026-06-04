# Customer Shopping Behavior Project

## Overview

This project demonstrates the complete data cleaning and preprocessing workflow performed on a Customer Shopping Behavior dataset using Python and Pandas. The cleaned dataset was then exported to PostgreSQL for further analysis and dashboard development.

The objective was to transform raw customer data into a structured and analysis-ready format by handling missing values, engineering new features, standardizing columns, and removing redundant information.

---

## Dataset Features

The dataset contains customer-related information such as:

* Age
* Gender
* Category
* Purchase Amount
* Review Rating
* Frequency of Purchases
* Subscription Status
* Discount Applied
* Promo Code Usage
* Previous Purchases

---

## Tools & Technologies

* Python
* Pandas
* PostgreSQL
* SQLAlchemy
* Psycopg2
* Jupyter Notebook

---

## Data Cleaning Steps

### 1. Data Exploration

* Loaded the dataset using Pandas.
* Inspected data types and dataset structure.
* Generated summary statistics.

### 2. Missing Value Treatment

* Identified missing values across all columns.
* Filled missing values in the **Review Rating** column using the median rating within each product category.

### 3. Column Standardization

* Converted all column names to lowercase.
* Replaced spaces with underscores.
* Renamed columns for better readability and SQL compatibility.

### 4. Feature Engineering

#### Age Group Creation

Created a new feature called **age_group** using quartile-based segmentation:

* Young Adults
* Adults
* Middle-aged
* Seniors

#### Purchase Frequency Conversion

Converted categorical purchase frequency values into numerical day equivalents:

| Frequency   | Days |
| ----------- | ---- |
| Weekly      | 7    |
| Fortnightly | 14   |
| Monthly     | 30   |
| Quarterly   | 90   |
| Annually    | 365  |

### 5. Redundancy Removal

* Compared `discount_applied` and `promo_code_used`.
* Identified both columns contained identical information.
* Removed the redundant `promo_code_used` column.

---

## PostgreSQL Integration

The cleaned dataset was successfully exported to PostgreSQL using SQLAlchemy.

### Database Workflow

1. Create PostgreSQL connection
2. Connect using SQLAlchemy Engine
3. Export cleaned DataFrame to PostgreSQL table
4. Prepare data for SQL analysis and dashboarding

---

## Project Outcomes

✔ Handled missing values

✔ Standardized column names

✔ Created customer age segments

✔ Converted purchase frequencies into numerical values

✔ Removed duplicate information

✔ Prepared dataset for analytics

✔ Exported cleaned data to PostgreSQL

---

## Future Enhancements

* Exploratory Data Analysis (EDA)
* Tableau Dashboard Development
* Customer Segmentation Analysis
* Predictive Analytics
* Machine Learning Models

---

## Project Structure

```text
Customer-Shopping-Behavior/
│
├── Customer_Shopping_Behaviour.ipynb
├── customer_shopping_behavior.csv
├── README.md
│
└── PostgreSQL Database
