---
title: "Add Columns to a Table (SSAS Tabular) | Microsoft Docs"
ms.custom: ""
ms.date: "03/01/2017"
ms.prod: analysis-services
ms.prod_service: "analysis-services, azure-analysis-services"
ms.service: ""
ms.component: ""
ms.reviewer: ""
ms.suite: "pro-bi"
ms.technology: 
  
ms.component: multidimensional-tabular
ms.component: data-mining
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 5974a3cc-caf8-4558-8836-6e3c24b1ee23
caps.latest.revision: 11
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
ms.workload: "On Demand"
---
# Add Columns to a Table (SSAS Tabular)
[!INCLUDE[ssas-appliesto-sqlas-aas](../../includes/ssas-appliesto-sqlas-aas.md)]
  This topic describes how to add columns to an existing table.  
  
## Add Columns from the Data Source  
 When using the Table Import Wizard to import data from a data source table, a new table is created in the model which includes all of the columns in the source table, or if you choose to filter out certain columns by using the Preview and Filter feature, only those columns and filtered data you select. You can also write a SQL Query that specifies only certain columns to import. You may, however, later determine a source table has additional columns that you want to add to the model table, or you need to add a calculated column with values derived from a DAX formula.  
  
 If, for example, when you initially imported from a data source, you used the Preview and Filter feature in the Table Import Wizard to select a limited number of columns from the source table, you later determine that you need to add another column that exists at the source table, but does not yet exist in the model table. Or, for example, a new AdjustedProfit column was added to the FactSales table at the data source, and you now want to add the same AdjustedProfit column and data to the Sales table in the model.  
  
 In these cases, you can use the Edit Table Properties dialog box to select columns from the source table and add them to the model table. The Edit Table Properties dialog box includes the table preview window. The table preview window displays the table at the source. Columns that are already included in the model table definition are already checked. Those columns that are not already included in the model table definition are not checked. You can add columns from the source to the model table definition by selecting the column and clicking OK. The table preview window in the Edit Table Properties dialog box provides the same view and features as the table preview window in the Preview and Filter page of the Table Import Wizard.  
  
> [!IMPORTANT]  
>  When adding a column to a table that contains two or more partitions, before adding the column to the table definition by using the Edit Table Properties dialog box, you must first use Partition Manager to add the column to all defined partitions. After you have added the column to the defined partitions, you can then add the same column to the table definition by using the Edit Table Properties dialog box.  
  
> [!NOTE]  
>  If you used a SQL Query to select tables and columns when you initially used the Table Import Wizard to import data, you must again use a SQL Query in the Edit Table Properties dialog box to add columns to the model table.  
  
#### To add a column from the data source by using the Edit Table Properties dialog box  
  
1.  In the model designer, click on the table you want to add a column to, then click the **Table** menu, and then click  **Table Properties**.  
  
2.  In the **Edit Table Properties** dialog box, in the table preview window, select the source column you want to add, and then click OK. Columns already included in the table definition will already be checked.  
  
## Add a Calculated Column  
 In a calculated column, a DAX formula is used to define a value for each row. For example, you can create a calculated column with a simple formula (=1) that adds a value of 1 to each row. Calculated columns can also have more complex formulas that calculate values based on other data in the model. Calculated columns are covered in more detail in other topics. For more information, see [Calculated Columns &#40;SSAS Tabular&#41;](../../analysis-services/tabular-models/ssas-calculated-columns.md).  
  
#### To create a calculated column  
  
1.  In the model designer, in Data View, select the table to which you want to add a new, blank calculated column, scroll to the right-most column, or click the **Column** menu, and then click **Add Column**.  
  
     To create a new column between two existing columns, right-click on an existing column, and then click **Insert Column**.  
  
2.  In the formula bar, type a DAX formula to add attributes for each row.  
  
## Add a Blank Column  
 You can create a named, blank column in a model table. Blank columns can be useful if you want to paste data from another source. Keep in-mind that pasted data is stored differently than imported data. For more information, see [Copy and Paste Data &#40;SSAS Tabular&#41;](../../analysis-services/tabular-models/ssas-import-data-copy-and-paste-data.md).  
  
#### To create a named, blank column  
  
1.  In the model designer, in Data View, select the table to which you want to add a blank column, scroll to the right-most column, or click the **Column** menu, and then click **Add Column**.  
  
     To create a new column between two existing columns, right-click an existing column, and then click **Insert Column**.  
  
2.  Click on the top cell, then type a name, and then press ENTER.  
  
## See Also  
 [Edit Table Properties Dialog Box &#40;SSAS&#41;](http://msdn.microsoft.com/library/8d913e83-7246-44cc-8fc7-31729023c0d8)   
 [Change table, column, or row filter mappings &#40;SSAS Tabular&#41;](../../analysis-services/tabular-models/change-table-column-or-row-filter-mappings-ssas-tabular.md)  
  
  
