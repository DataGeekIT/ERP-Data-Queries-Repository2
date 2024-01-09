# ERP-Data-Queries-Repository2


This SQL code appears to be a SELECT statement retrieving data from a table named twhinr1101000 with an alias wh. The code selects various columns and performs some transformations on the data. Here's a breakdown:

Selected Columns:

LTRIM(wh.t_item) AS 'Item'
wh.t_cwar AS 'Warehouse'
wh.t_trdt AS 'Transaction Date'
wh.t_seqn AS 'Sequence'
wh.t_ocmp AS 'Order Company'
wh.t_koor AS 'Type of Order'
'Type of Order Desc' = (SELECT top(1) ...)
wh.t_orno AS 'Order'
wh.t_pono AS 'Order Line'
wh.t_srnb AS 'Order Sequence'
wh.t_itid AS 'Transaction ID'
wh.t_qstk AS 'Quantity'
wh.t_kost AS 'Transaction Type'
'Transaction Type Desc' = (SELECT top(1) ...)
wh.t_site AS 'Site'
wh.t_rcno AS 'Receipt'
wh.t_shpm AS 'Shipment'
wh.t_bpid AS 'Business Partner'
'Internal transfer' = CASE ... END
Subqueries:

Two subqueries are used to retrieve the description for 'Type of Order' and 'Transaction Type' based on certain conditions from tables erplndb.dbo.tttadv401000 and erplndb.dbo.tttadv140000.
The results of these subqueries are assigned to the columns 'Type of Order Desc' and 'Transaction Type Desc' respectively.
Case Statement:

There is a CASE statement labeled as 'Internal transfer' that checks conditions on the wh.t_sfsi and wh.t_stsi columns from the table twhinh2001000 (aliased as whinh200). Based on these conditions, it returns 'Yes' or 'No'. This case statement seems to be determining whether it's an internal transfer.
Table and Alias:

The data is selected from the table twhinr1101000 with the alias wh.
In summary, the code retrieves various columns from the table twhinr1101000, performs some data transformations using subqueries to fetch descriptions based on conditions, and includes a case statement to determine if it's an internal transfer. The data is filtered and manipulated based on the specified conditions in the subqueries and case statement.





