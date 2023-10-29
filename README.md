### Case Study Title: "AdventureWorks Sales Data Analysis with Power BI"-Data Modelling

Abstract:
This case study focuses on using Power BI to empower AdventureWorks, a leading software company, by building a comprehensive sales report. We will connect to the AdventureWorks Sales Data, create relationships, import data, and add calculated columns to enhance data analysis. The report will enable informed business decisions based on sales data.

Introduction:
AdventureWorks is a prominent software company looking to harness the power of data analysis to enhance its business decisions. We will utilize Power BI, a leading business intelligence tool, to extract insights from sales data and present it in a meaningful way.

Methodology:

a) Data Source Connection:
We start by connecting to the AdventureWorks Sales Data stored in the 'AdventureWorks Sales Data.xlsx' file. This dataset contains multiple worksheets, including DimCurrency, DimCustomer, DimDate, DimProduct, DimPromotion, DimSalesTerritory, and FactInternetSales.

b) Data Import:
We import the relevant worksheets, including DimCurrency, DimCustomer, DimDate, DimProduct, DimPromotion, DimSalesTerritory, and FactInternetSales.

c) Creating Relationships:

We create a relationship between the FactInternetSales table's OrderDateKey column and the DateKey column in DimDate, with a cardinality of Many to One (*:1), cross-filter direction set to Single, and making this relationship Active.
Relationships are established between FactInternetSales DueDateKey and DimDate DateKey, and between FactInternetSales ShipDateKey and DimDate DateKey.
f) Data Import from External Source:
We load data from the 'AdventureWorks Product Categories.xlsx' file, specifically the DimProductCategory and DimProductSubcategory data.

g) Relationship Modification:
The relationship between DimProductCategory and DimProductSubcategory is deleted.

h) Relationship Creation:

We create a Many to One (*:1) relationship between DimProductSubcategory's CategoryKey and DimProductCategory's CategoryKey with the cross-filter direction set to Both.
Another Many to One (*:1) relationship is created between DimProduct's ProductSubcategoryKey and DimProductSubcategory's SubcategoryKey with the cross-filter direction set to Both.
j) Calculated Column - IncomeStatus:
We add a calculated column named "IncomeStatus" to the DimCustomer table based on the YearlyIncome column. Income is classified into categories: Lower Income, Middle Income, Higher Income, and Very High Income.

k) Calculated Column - DaysSinceFirstPurchase:
A calculated column named "DaysSinceFirstPurchase" is added to the DimCustomer table to show the number of days since a customer made their first purchase.

l) Calculated Column - FullName:
We create a calculated column named "FullName" in the DimCustomer table, which concatenates the FirstName and LastName of each customer.

m) Calculated Column - MaleFemale:
A calculated column named "MaleFemale" is added to the DimCustomer table, which converts the values of the Gender column to Male or Female.

n) Calculated Column - Relationship:
We add a calculated column to the DimCustomer table, called "Relationship," which converts the value of the MaritalStatus column to Married or Single.

o) Calculated Column - MainCategory:
A calculated column named "MainCategory" is added to the DimProductSubcategory table, which gets the category name from DimProductCategory.

q) Customer-Product Details:
For each customer, we display the product details they have bought, allowing for a comprehensive understanding of customer preferences and behavior.

p) Calculated Column - PromotionLengthDays:
A calculated column named "PromotionLengthDays" is added to the DimPromotion table, which calculates the difference between StartDate and EndDate.

Conclusion:
This case study demonstrates how Power BI can be used to extract valuable insights from complex datasets and empower a leading software company like AdventureWorks. By establishing relationships, importing data, and adding calculated columns, we have created a powerful tool for business decision-making based on sales data. The generated reports will provide valuable insights into customer behavior, product preferences, and promotion effectiveness.
