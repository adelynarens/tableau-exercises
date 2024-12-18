# Data Analytics For Business Professionals: Tableau

## Part I: Warm-Up 

These exercises are repeats from the first class, but will give you an opportunity to work with Tableau on your own and reinforce the material we covered.

1. Change the type of `Item ID`, `Customer ID`, and `Order ID` from Number to String.
##

2. Split the `Customer Name` field into a `Customer First Name` and `Customer Last Name` field. Hide the original `Customer Name` field. 
##

3. Create a bar chart showing the total `Sales` by `Department` and `Region`.
* Add data labels to the bar
* Format the y-axis to currency

![alt text](/images/alternate%20exercise/1.3.png)
##

4. Create a line chart that shows `Sales` by month. Use `Order Date` and the continuous version of months.

![alt text](/images/alternate%20exercise/1.4.png)
##

5. Create a dual-axis line chart that shows `Sales` and `Profit` by quarter. Make sure to synchronize the axes. 

![alt text](/images/alternate%20exercise/1.5.png)
##

6. Create a geographic map that shows the number of `Sales` by `State`.

![alt text](/images/alternate%20exercise/1.6.png)
##

7. Create a dashboard to display the visualizations. You may find it helpful to rewatch the video from last class: https://www.tableau.com/learn/tutorials/on-demand/getting-started-part9?playlist=509087 

Please be prepared to present your dashboard.
##

## Part II - Basic Visualizations
1. Create a horizontal bar chart that shows average `Sales` by `Category`. 
    - Add labels to display the exact sales values for each category
    - Sort the categories in descending order based on average sales
    - Format the axis and labels to currency

    ![Exercise 1](/images/exercise%201/1.1.png)
    ##

2. Create a line chart that shows `Orders (Count)` by month.
    - Format the dates to abbreviation and change the orientation to horizontal
    - Use the discrete version of months

     ![Exercise 2](/images/exercise%201/1.2.png)
     ##

3. Create a dual-axis chart that compares total `Sales` and `Profit` by `Ship Date` year.
    - Synchronize the axes
    - Hide the second vertical axis
    - Format the axis to currency
    - Use the continuous version of years
    - Remove the y-axis label

    ![Exercise 3](/images/exercise%201/1.3.png)
    ##

4. Create a geographic bubble chart that shows the median `Sales` by `State`.
    - Make the size of the bubble represent the median sales
    - Add the state name as a label

    ![Exercise 4](/images/exercise%201/1.4.png)
    ##

## Part III: Managing Metadata
1. Hide the `Row ID` field.

This field was incorrectly interpreted as a date by Tableau when imported. Try changing the field type to a String (it doesn't work!). We need more advanced tools such as Tableau Prep to fix this, but for now, we will just hide it.
##

2. Add the following data source filters:

* `Order Date` should be between 1/1/2014 and 1/1/2014
* Filter out orders with very low sales (`Sales` <= $10)
* Limit the data to the South and East `Region`.
##
3. Create an extract and add a filter that includes only orders with `Profit` >= $0.

Note: Tableau doesn't query the data because it's directly connected to the Excel file you provided. This means both data source and extract filters are applied at the same time, as Tableau is working with the data already loaded.
##
 
4. Rename ambiguous field names to more descriptive ones:

* Rename `Category` to `Product Category`
##

5. Create a calculated field called `Profit Margin`.

Hint: (`Profit` / `Sales`)

##

6. Assign aliases for the labels in `Order Priorty`

* Low --> L
* Medium --> M
* High --> H
* Critical --> C
##

7. Create a Group for `Product Category` called `Product Category Groups`

![Exercise 2](/images/exercise%202/2.8.png)
##

8. Create a set using the `Customer Name` field called `Top 10 most profitable customers`.

The set should indicate for each record if the customer is in the Top 10 most profitable. 
##

9. Create a set using the `Customer Name` field called `Top 10 most frequent customers`.

The set should indicate for each record if the number of orders is in the top 10 for all customers. 

![Exercise 2](/images/exercise%202/2.10.png)

## Part IV - Data Analysis
1. Create a bar chart that shows the top 10 most profitable customers sorted by descending profit.**
Hint: Use the `Top 10 most profitable customers` set as a filter.

* Format the axis to currency
* Add labels to the end of the bars
* Hide field labels for rows

![Exercise 2](/images/exercise%202/2.12.png)
##

2. Create a Stacked Bar Chart to determine which categories perform best in different regions. Use the `Product Category Group` to color the bars.

* Make sure the axis is formated to currency

![Exercise 2](/images/exercise%202/2.13.png)
##


3. Visualize `Sales` contribution by `Customer Name` for the top 10 most frequent customers using a treemap. Color the boxes by `Profit` to help determine which frequent customers have low profitability.
Hint: Use Show Me

* Use the Red-Green Diverging color palette.

![Exercise 2](/images/exercise%202/2.14.png)
##

4. Create a highlight table to visualize average `Profit Margin` by `Order Priority`.** Hint: Use Show Me.

* Sort the `Order Priority` labels in order of priority.

* Use the color palette Sunrise-Sunset Diverging and reverse the palette so the lowest average profit margins are shown in red. 

* Format `Profit Margin` as a % with 1 decimal point.

Note: When we created the `Profit Margin` field in Part I, Tableau correctly infered that the field should be a percentage. However, adding a percentage to a visualization does not automatically include '%' and choosing the percentage format when making a visualization multiplies the number by 100 again, which is not what we want. This is an unfortunate feature of Tableau, but you will have to find one of several "hacks" to get the chart formatted correctly. 

![Exercise 2](/images/exercise%202/2.15.png)
##

5. Put everything together into a dashboard.

Use your best creative judgement to arrange the visualizations created in Part IV into a dashboard. Include the following: 

* Create a vertical container covering the entire view.

* Drag a text container to the top of the dashboard. Add the Title `Class 2: Superstore Sales Insights`. Set the font size to 28, bold the text, and change the text color to black.

* Change the background color of the dashboard to light grey.

* Add Outer Padding of 10 to all containers 

* Hide the legend for the `Frequent Customer Profitability` and `Profit Margin by Priority` visualizations. 



