# Food Delivery SQL Project

## Overview
This project is designed to help practice SQL queries using a food delivery database. The dataset represents orders received by a local food delivery company, and various queries are written to extract meaningful insights.

## Database Schema
The database is named `Orders` and consists of the following columns:

- `order_id` (INT) – Unique ID for each order
- `order_time` (DOUBLE) – Time the order was placed
- `customer_id` (VARCHAR) – Unique identifier for each customer
- `customer_name` (VARCHAR) – Name of the customer
- `address_pincode` (INT) – Pincode of the delivery address
- `apartment_floor` (INT) – Floor number of the apartment

## Queries Implemented

### 1. Retrieve Sample Data
```sql
SELECT * FROM Orders
LIMIT 3;
```

### 2. Distinct Pin Codes from Orders
```sql
SELECT DISTINCT address_pincode FROM Orders;
```

### 3. Orders Received Between 12 PM and 1 PM
```sql
SELECT * FROM Orders
WHERE order_time BETWEEN 12 AND 13;
```

### 4. Customers Whose Name Ends with 'a'
```sql
SELECT DISTINCT customer_id FROM Orders
WHERE customer_name LIKE '%a';
```

### 5. Orders Sorted by Apartment Floor (Ascending)
```sql
SELECT * FROM Orders
ORDER BY apartment_floor;
```

### 6. Orders with Missing Order Time
```sql
SELECT order_id FROM Orders
WHERE order_time IS NULL;
```

### 7. Corrected Query to Retrieve Specific Customers
```sql
SELECT DISTINCT customer_name
FROM Orders
WHERE (address_pincode = 122001 OR address_pincode = 122002)
AND order_time < 12.30
AND apartment_floor >= 3;
```

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/food-delivery-sql.git
   ```
2. Navigate to the project directory:
   ```bash
   cd food-delivery-sql
   ```
3. Execute the queries in a SQL environment.

## Author
[Dinesh Reddy V](https://github.com/your-username)

