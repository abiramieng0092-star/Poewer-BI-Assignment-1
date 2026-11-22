                   power BI Assignment Data Transformation & Data modeling                          

FILES IN THIS FOLDER:
    1. Power BI File (.pbix) - Contains all transformations and data model
    2. PDF Document (.pdf) - Contains screenshots and explanation
    3. README.txt - This file
    4. Raw data set
DATASETS USED:
    - List of Orders.csv
       Order ID, Order Date, Customer Name, City, State, Category, Amount, Profit
    - Order Details.csv
       Order ID, Category, Sub-Category, Quantity, Amount, Profit
    - Sales Target.csv
       Category, Month of Order Date, Target

TRANSFORMATIONS DONE:
     1. Imported all 3 datasets into Power BI
     2. List of Orders restricted to first 500 rows
     3. Order Date changed to Date type
     4. Amount and Target changed to Fixed Decimal Number
     5. CustomerName formatted to Proper Case
     6. City + State merged to Location (City, State)
     7. Custom Column: Profit Margin = Profit / Amount (Percentage)
     8. Conditional Column: Profit Status
         Profit < 0 = Loss
         Profit = 0 = Break-Even
         Profit > 0 = Profit
     9. Merged List of Orders + Order Details using Order ID = Orders Data
        Join Type: Left Outer Join
    10. Missing values checked, duplicates removed
    11. Sorted Orders Data by Order Date - Descending
    12. Filtered for Tamil Nadu
    13. Grouping:
          - Order Details: Count of Order ID, Avg Profit by Category, Total Amount by Sub-Category
          - Sales Target: Total Target by Month

DATA MODELING:
          - List of Orders -> Order Details using Order ID
          - Order Details -> Sales Target using Category
          - All relationships are Active, checked in Manage Relationships

INSIGHTS:
          1. Tamil Nadu data is filtered and analysed separately for clear regional understanding.
          2. Profit Status column clearly separates Profit, Loss and Break-Even orders.
          3. Profit Margin helps to understand which orders are more profitable.
          4. Grouping by Category and Sub-Category shows which category gives more Total Amount and Average Profit.
          5. Grouping Sales Target by Month helps to compare Target vs Actual Sales.
          6. Data Modeling with proper relationships ensures accurate analysis across all 3 tables.

HOW TO OPEN:
          1. Open .pbix file in Power BI Desktop
          2. Go to Power Query Editor to see all transformation steps
          3. Go to Model View to see relationships
