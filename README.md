# QWT Dashboard
### Problem Statement
This dashboard is designed to provide comprehensive insights into QWT metrics (Quality, Wait Time, and Throughput). It aids businesses in identifying performance gaps, optimizing workflows, and improving overall efficiency by analyzing key metrics. Understanding these aspects allows businesses to enhance their operations, reduce delays, and improve customer satisfaction.

#### Data Used:-
The project involves the following 13 tables:

* Categories: Category ID, Category Name, Description
* Customers: Customer ID, Company Name, Contact Name, City, Division, Address, Fax, Phone, Postal Code, State/Province
* Divisions: Division ID, Division Name
* Employee Budget: Employee ID, Target per Employee
* Employees: Employee ID, Last Name, First Name, Title, Hire Date, Office Date, Office, Extension, Reports To, Yearly Salary
* Offices: Office, Office Address, Office Postal Code, Office City, Office State/Province, Office Phone, Office Fax, Office Country
* Order Details: Order ID, Line No, Product ID, Quantity, Unit Price, Discount, Line Sales Amount, Margin, Discounted Amount
* Orders: Order ID, Order Date, Customer ID, Employee ID, Shipper ID, Freight
* Products: Product ID, Product Name, Supplier ID, Category ID, Quantity per Unit Cost, Unit Price, Units in Stock, Units on Order
* Shipment: Order ID, Line No, Shipper ID, Customer ID, Product ID, Employee ID, Shipment Date
* Shippers: Shipper ID, Company Name
* Suppliers: Supplier ID, Company Name, Contact Name, Address, City, Postal Code, Country, Phone, Fax
* Yearly Budget: Year, Target per Year
### Steps :-
#### Step 1: Data Preparation and Transformation
* Create a Fact Table: Merged the Order Details, Orders, and Shipments tables to form a comprehensive fact table. Since we do not have a received order date or return date, the minimum shipment date for each order was used as a proxy.

* Product Data Merging: Merged the Products, Categories, and Suppliers tables based on their respective keys to form a detailed product dimension table.

* Customer and Division Merging: Merged the Customers and Divisions tables to include customer-specific details along with their respective divisions.

* Employee Data Merging: Merged the Employees, Employee Budget, and Offices tables to create a dimension table that includes employee details, budget targets, and office locations.

* Fiscal Date Table Creation: Created a Fiscal Date Table running from April to March based on the existing dates to accommodate financial year analysis.

* Units Conversion: Developed a unit conversion table to standardize different units across products, ensuring consistency in analysis.

#### Step 2: Dynamic Measures and Analysis
* Dynamic Selector Creation: Implemented a dynamic selector in Power BI that allows users to switch between analyzing revenue and margin, providing flexibility for comprehensive analysis.

* DAX Measures: Calculated various DAX measures to derive meaningful insights from the data, such as Quality Scores, Wait Times, and Throughput Rates.

#### Step 3: Data visualizations

* Created various visualizations, including bar charts, line graphs, and KPIs, to represent key QWT metrics like Average Wait Time, Throughput Rate, and Quality Score.

* Added slicers and filters to allow users to drill down into specific areas, such as viewing performance by route or analyzing throughput rates by product category.


#Snapshots of Dashboard
![image](https://github.com/user-attachments/assets/477011b1-b646-442b-8d2b-32ed5c4f3122)
![image](https://github.com/user-attachments/assets/fc0a06cb-2474-4c86-b907-db33f756b626)
![image](https://github.com/user-attachments/assets/db431b0f-fde0-4565-b092-beb494288056)
![image](https://github.com/user-attachments/assets/d550e770-cd91-4b5b-97ba-dbaa4d33d2e3)





