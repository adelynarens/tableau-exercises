# Data Analytics For Business Professionals: Tableau
## Class #2: Connecting to Data in Tableau

### Part I: Preparing the dataset 
##

**1. Create a new Tableau workbook and initiate a live connection to the following data. Drag the Orders Table to the canvas**:
https://docs.google.com/spreadsheets/d/1YUZ1UnryuCX7cwbfNptGuzx0G4yth7i-m9Jrkce9_PE/edit?usp=sharing.

Note: If you do not have a Google account, you can also download the Excel data file [here](/data/Superstore.xlsx). 
##

**2. Change the `Customer ID` and `Order ID` field from type Number to type String.**

Always make this your first step when cleaning data. We never want to accidentally perform math on an ID field and Strings take up less space than Numbers in memory. 
##

**3. Hide the `Row ID` field.**

This field was incorrectly interpreted as a date by Tableau when imported. Try changing the field type to a String or a Number (it doesn't work!). We need more advanced tools such as Tableau Prep to fix this. For now, we will just hide it.
##

**4. Add the following data source filters:**

* `Order Date` should be between 1/1/2014 and 1/1/2014
* Filter out orders with very low sales (`Sales` <= $10)
* Limit the data to the South and East `Region`.
##
**5. Create an extract filter that includes only orders with `Profit` >= $0.**
##

**6. Rename ambiguous field names to more descriptive ones**:

* Rename `Sub-Category` to `Product Sub-Category`
* Rename `Category` to `Product Category`
##

**7. Create a calculated field called `Profit Margin`.**

(`Profit` / `Sales`)

##

**8. Create a Group for `Product Category` called `Category Groups`**

![Exercise 2](/images/exercise%202/2.8.png)

**9. Create a set using the `Customer Name` field called `Top 10 most profitable customers`.**

The set should indicate for each record if the customer is in the Top 10 most profitable. 
##

**10. Create a set using the `Customer Name` field called `Top 10 most frequent customers`.**

The set should indicate for each record if the number of orders is in the top 10 for all customers. 

![Exercise 2](/images/exercise%202/2.10.png)

