# Aggregations

```
CREATE TABLE Products (
    ProductID INT PRIMARY KEY,
    ProductName VARCHAR(100) NOT NULL,
    Category VARCHAR(50) NOT NULL,
    Price DECIMAL(10, 2) NOT NULL,
    StockQuantity INT NOT NULL
);

INSERT INTO Products (ProductID, ProductName, Category, Price, StockQuantity) VALUES
(1, 'Laptop Pro', 'Electronics', 1200.00, 50),
(2, 'Gaming Mouse', 'Electronics', 75.50, 150),
(3, 'Mechanical Keyboard', 'Electronics', 120.00, 80),
(4, 'Desk Chair Ergo', 'Furniture', 250.00, 30),
(5, 'Office Desk', 'Furniture', 350.00, 20),
(6, 'Smart Speaker', 'Electronics', 99.99, 100),
(7, 'Coffee Table', 'Furniture', 180.00, 45),
(8, 'LED Monitor', 'Electronics', 250.00, 70),
(9, 'Bookcase Small', 'Furniture', 85.00, 60),
(10, 'Wireless Earbuds', 'Electronics', 150.00, 200);
```
