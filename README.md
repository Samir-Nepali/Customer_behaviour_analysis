# Customer_behaviour_analysis
Customer Behaviour Data Analysis Using Python, Sql and Power Bi

## Project Overview 
This project analyzes customer shopping behaviour using transactional data from 3,900 purchases across various product categories. The goal is to uncover insights into spending patterns, customer segments, product preferences, and subscription behaviour to guide strategic business decisions.

## Dataset Summary
- **Customer Demographics**:Age, Gender,Location,Subscription Status.
- **Purchase details**:Item Purchased, Category, Purchase Amount, Season, Size, Color.
- **Shopping details**:Discount Applied, Promo Code, Previous Purchases, Frequency of purchases, Review rating , Shipping type.
-**Missing data**: 37 values in review rating column 

## Exploratory Data Analysis using Python
- **Data loading**: Imported datasets using pandas.
-**Initial Exploration**: Used df.info() to check structure and .describe() for summary statistics.
-**Missing data handling**: Checked for null values (df.isnull().sum()) and imputed missing values in the Review Rating column using median rating of each product category.
(df['Review Rating']= df.groupby('Category') ['Review Rating'].transform(lambda x: x.fillna(x.median())))
-**Column Standardization**: Renamed columns to make snake case for better readability and documentation.
