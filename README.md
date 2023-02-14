# AW_Report_PowerBI
Sales Report from AdventureWorks using Power BI and SSAS Tabular Cube.

We used live connection to SSAS Tabular model (Refer to SSAS_Tabular_Cube repository for Tabular model creation from AdvatureWorks DW database.).

All calculated columns and measure came directly from tabular cube. 2 visualization level measures are created in Power BI.

BestSellingProduct = VAR Ranking = VALUES(DimProduct[EnglishProductName]) RETURN CALCULATE( [InternetTotalSales], TOPN(1, ALL(DimProduct[EnglishProductName]), [InternetTotalSales]), Ranking )

BestSellingCity = VAR Ranking_City = VALUES(DimGeography[City]) RETURN CALCULATE( [InternetTotalSales], TOPN(1, ALL(DimGeography[City]), [InternetTotalSales]), Ranking_City )

<img width="911" alt="Overview" src="https://user-images.githubusercontent.com/118220804/218331813-a213608a-277e-4fee-952a-40fba3c46c51.png">

<img width="912" alt="Product" src="https://user-images.githubusercontent.com/118220804/218331817-68040af6-a562-4d7d-a893-55bd97f036db.png">

<img width="913" alt="Region" src="https://user-images.githubusercontent.com/118220804/218331823-4685d8d3-0fc1-4ba3-b866-05badc7a9d33.png">
