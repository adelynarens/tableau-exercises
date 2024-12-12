# Data Analytics For Business Professionals: Tableau
## Class #2: Connecting to Data in Tableau

### Part I: Preparing the dataset 
##

**1. Create a new Tableau workbook and initiate a live connection to the following data. Drag the Orders Table to the canvas**:
https://docs.google.com/spreadsheets/d/1YUZ1UnryuCX7cwbfNptGuzx0G4yth7i-m9Jrkce9_PE/edit?usp=sharing.

Note: If you do not have a Google account, you can also download the Excel data file [here](/data/Superstore.xlsx). 
##

**2. Change the `Customer ID`, `Item ID`, and `Order ID` field from type Number to type String.**

Always make this your first step when cleaning data. We never want to accidentally perform math on an ID field and Strings take up less space than Numbers in memory. 
##

**3. Hide the `Row ID` field.**

This field was incorrectly interpreted as a date by Tableau when imported. Try changing the field type to a String (it doesn't work!). We need more advanced tools such as Tableau Prep to fix this, but for now, we will just hide it.
##

**4. Add the following data source filters:**

* `Order Date` should be between 1/1/2014 and 1/1/2014
* Filter out orders with very low sales (`Sales` <= $10)
* Limit the data to the South and East `Region`.
##
**5. Create an extract and add a filter that includes only orders with `Profit` >= $0.**
##

Note: If you connected through the Excel file, both data source and extract filters perform the filtering at the same time. 

**6. Rename ambiguous field names to more descriptive ones**:

* Rename `Category` to `Product Category`
##

**7. Create a calculated field called `Profit Margin`.**

Hint: (`Profit` / `Sales`)

##

**8. Assign aliases for the labels in `Order Priorty`** 

* Low --> L
* Medium --> M
* High --> H
* Critical --> C
##

**9. Create a Group for `Product Category` called `Product Category Groups`**

![Exercise 2](/images/exercise%202/2.8.png)
##

**10. Create a set using the `Customer Name` field called `Top 10 most profitable customers`.**

The set should indicate for each record if the customer is in the Top 10 most profitable. 
##

**11. Create a set using the `Customer Name` field called `Top 10 most frequent customers`.**

The set should indicate for each record if the number of orders is in the top 10 for all customers. 

![Exercise 2](/images/exercise%202/2.10.png)

### Part II: Data Analysis
##

**12. Create a bar chart that shows the top 10 most profitable customers sorted by descending profit.**
Hint: Use the `Top 10 most profitable customers` set as a filter.

* Format the axis to currency
* Add labels to the end of the bars
* Hide field labels for rows

![Exercise 2](/images/exercise%202/2.12.png)
##

**13. Create a Stacked Bar Chart to determine which categories perform best in different regions. Use the `Product Category Group` to color the bars.**

* Make sure the axis is formated to currency

![Exercise 2](/images/exercise%202/2.13.png)
##


**14. Visualize `Sales` contribution by `Customer Name` for the top 10 most frequent customers using a treemap. Color the boxes by `Profit` to help determine which frequent customers have low profitability.** 
Hint: Use Show Me

* Use the Red-Green Diverging color palette.

![Exercise 2](/images/exercise%202/2.14.png)
##

**15. Create a highlight table to visualize average `Profit Margin` by `Order Priority`.** Hint: Use Show Me.

* Sort the `Order Priority` labels in order of priority.

* Use the color palette Sunrise-Sunset Diverging and reverse the palette so the lowest average profit margins are shown in red. 

* Format `Profit Margin` as a % with 1 decimal point.

Note: When we created the `Profit Margin` field in Part I, Tableau correctly infered that the field should be a percentage. However, adding a percentage to a visualization does not automatically include '%' and choosing the percentage format when making a visualization multiplies the number by 100 again, which is not what we want. This is an unfortunate feature of Tableau, but you will have to find one of several "hacks" to get the chart formatted correctly. 

![Exercise 2](/images/exercise%202/2.15.png)
##

**16. Put everything together into a dashboard.**

Use your best creative judgement to arrange the visualizations created in Part II of this exercise into a dashboard. Include the following: 

* Create a vertical container covering the entire view.

* Drag a text container to the top of the dashboard. Add the Title `Class 2: Superstore Sales Insights`. Set the font size to 28, bold the text, and change the text color to black.

* Change the background color of the dashboard to light grey.

* Add Outer Padding of 10 to all containers 

* Hide the legend for the `Frequent Customer Profitability` and `Profit Margin by Priority` visualizations. 



