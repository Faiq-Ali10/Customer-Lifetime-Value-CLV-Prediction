# Customer Lifetime Value (CLV) Prediction

This project aims to predict Customer Lifetime Value (CLV) using RFM (Recency, Frequency, and Monetary) analysis. The project involves analyzing transactional data, calculating RFM metrics, and predicting customer behavior using machine learning models. The dataset used for the project includes transaction details, customer information, and the corresponding product details.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset Description](#dataset-description)
- [Data Processing](#data-processing)
- [Feature Engineering](#feature-engineering)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Usage](#usage)
- [Contributors](#contributors)
- [License](#license)

## Project Overview
The goal of this project is to predict Customer Lifetime Value (CLV) for each customer using historical transaction data. CLV prediction can help businesses target the right customers, enhance retention strategies, and optimize marketing efforts.

This project consists of the following steps:
- **Data Cleaning**: Handling missing values and removing duplicates.
- **Feature Engineering**: Calculation of RFM metrics and transformations for the target prediction.
- **Model Training**: Using machine learning models to predict CLV.
- **Evaluation**: Analyzing the model's performance using metrics such as Mean Squared Error (MSE) and R-squared.

## Dataset Description

The dataset used in this project consists of the following columns:

| Variable Name | Role       | Type       | Description                                                       | Units   | Missing Values |
|---------------|------------|------------|-------------------------------------------------------------------|---------|----------------|
| `InvoiceNo`   | ID         | Categorical | A 6-digit integral number uniquely assigned to each transaction. If this code starts with letter 'c', it indicates a cancellation. | -       | No             |
| `StockCode`   | ID         | Categorical | A 5-digit integral number uniquely assigned to each distinct product. | -       | No             |
| `Description` | Feature    | Categorical | Product name.                                                     | -       | No             |
| `Quantity`    | Feature    | Integer     | The quantities of each product (item) per transaction.           | -       | No             |
| `InvoiceDate` | Feature    | Date        | The day and time when each transaction was generated.             | -       | No             |
| `UnitPrice`   | Feature    | Continuous  | Product price per unit (in sterling).                             | Sterling | No             |
| `CustomerID`  | Feature    | Categorical | A 5-digit integral number uniquely assigned to each customer.     | -       | No             |
| `Country`     | Feature    | Categorical | The name of the country where each customer resides.              | -       | No             |

## Data Processing
1. **Loading the Data**: The data is loaded from CSV files using pandas.
2. **Data Cleaning**: Removed rows with cancellations and missing values.
3. **Feature Engineering**: Calculated RFM metrics (Recency, Frequency, and Monetary values) for each customer based on their transaction history.

## Feature Engineering
The following features were created to analyze customer behavior:
- **Recency**: The number of days since the customer's last purchase.
- **Frequency**: The total number of transactions made by the customer.
- **Monetary Value**: The total value spent by the customer.

These features were used to build a machine learning model that predicts the **Customer Lifetime Value (CLV)**.

## Modeling
We used the following machine learning models to predict CLV:
- **Linear Regression**: A simple regression model to predict the CLV based on RFM metrics.
- **Random Forest**: A more complex model to improve prediction accuracy.

### Model Performance
- **Mean Squared Error (MSE)**: 0.0013
- **R-squared**: 0.9993

These metrics indicate that the model performs well and can effectively predict the CLV of customers.

## Evaluation
The performance of the model was evaluated using **Mean Squared Error (MSE)** and **R-squared**. The model achieved a high R-squared score, indicating a strong correlation between the predicted and actual CLV.

## Usage
To run the project on your local machine:
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/clv-prediction.git
