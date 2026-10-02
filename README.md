This project focuses on preparing NorthPoint Retail data using Power BI. The main objective is to clean, transform, and organize data for accurate sales analysis and business decision-making.

2. Tools Used
•	Power BI Desktop: Used to prepare and model the data.
•	Power Query Editor: Used for data cleaning and transformation.
•	Model View: Used to create relationships between tables.

4. Data Cleaning and Transformation
- Data Import: Imported sales, product, customer, store, salesperson, returns, targets, exchange rates, and calendar data into Power BI.
- Combine Files: Combined 24 monthly sales CSV files using the Folder connector to create one sales table.
- Data Profiling: Checked column quality, distribution, errors, and missing values to understand the condition of the data.
- Remove Duplicates: Removed duplicate product and customer records using their unique keys.
- Handle Missing Values: Checked missing values and corrected or handled them where required.
- Text Standardization: Cleaned text fields and standardized inconsistent values in product and customer data.
- Change Data Types: Corrected data types for dates, numbers, and other columns to ensure accurate calculations.
- Merge Queries: Combined related tables to bring required information together for analysis.
- Handle Returns: Connected return records with sales orders and identified return records that did not match any sales order.
- Unpivot Targets: Converted the store targets table from a wide format into a structured table with separate rows for each store and month.
- Prepare Date Table: Organized the calendar data and prepared date-related fields for time-based analysis.
- Organize Queries: Grouped queries into suitable categories and disabled loading for staging and checking queries that were not required in the final model.
4. Data Modeling
- Create Fact Tables: Prepared FactSales for sales transactions and FactTargets for monthly store targets.
- Create Dimension Tables: Prepared DimDate, DimProduct, DimCustomer, DimStore, and DimSalesPerson to provide descriptive information for analysis.
- Create Relationships: Connected fact and dimension tables using a star-schema model with appropriate many-to-one relationships.
-Create hierarchies: Product (Category > SubCategory > Product Name), Geography (Region > State > City > StoreName), Date (Year > Quarter > MonthNameShort > Date).
-Set Sort By Column: MonthNameShort sorted by MonthNumber, MonthYear sorted by MonthYearSort, WeekdayName sorted by WeekdayNumber.
-Set data categories: City to City, State to State/Province.


- Model Formatting: Organized the model by hiding unnecessary key columns, setting month and weekday sorting, creating hierarchies, and marking the date table.
Set Summarization FOR  Do Not Summarize on every column that should never be added up, especially Year and any numeric code.

