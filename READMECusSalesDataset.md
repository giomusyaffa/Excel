# Step-by-step Analysis of The Customer Sales Dataset 🖥️
## Overview 📘
This project analyzes customer sales data to uncover key trends, product performance, and customer behavior. The goal is to transform raw transactional data into actionable insights using Microsoft Excel’s **advanced formulas**, **PivotTables**, and **data visualization tools**.
## Dataset Description ✍️
- Customer Name : Buyer's name
- Purchase Date : The date of an item sold (dd/mm/yy)
- Product Category : Variation of items (Books, Clothing, Groceries, Electronics)
- Sale : The cost of an item
- Quantitiy : Sum of the items sold
- Discount Applied : True / False
- Purchase Month : Showed as a numerical value (1: January, etc)
- Purchase Day and Year : Showed as a numerical value
- Price : Final cost of an item
### Step 1
#### **Transforming raw data**
The first step in analyzing a data, especially when acquiring it from an open source data like **Kaggle** is to transform the raw data.

Usually when you download a dataset in a .csv format you would see something like this:

<img src="https://i.imgur.com/c5N23nJ.png" align= "center" height="80%" width="80%"/>

To seperate it into each columns, all you have to do is convert text to columns in the **Data** menu and choose delimeted, with *comma* as the delimiters (since the values are seperated by a comma):

<img src="https://i.imgur.com/V0tu9AR.png" align= "center" height="80%" width="80%"/>

Finally you have your readable, ready-to-analyze data:

<img src="https://i.imgur.com/nQbfdjy.png" align= "center" height="80%" width="80%"/>

### Step 2
#### 1. PivotTables & PivortChart
The easiest way to interpret and analyze large amounts of data without using any complicated functions is by using this interactive tool.

By using **PivotTables** we can choose specific fields from our data and categorize it to each respective columns and values

Let's say you want to know if by discounting a product will boost sales, you can do that by selecting **Product Category** and **Discount Applied** to the rows field and **Quantity** to the values field.

<img src="https://i.imgur.com/UA5YEH4.png" align= "center" height="80%" width="80%"/>

As you can see from the PivotTables above, a boost of sales after applying discount only happens to **books**, and **electronics** while **groceries** are unaffected and **clothing** shows a **decline** in sales.

Okay, let's do another one, now this is a little complicated than before, but what if you want to see the sales pattern of each product in 6 months?

You can do that by selecting **Product Category** to the Columns field, **Purchase Month** to the rows field, and **Quantity** to the values field. And the PivotTables would look like this:

<img src="https://i.imgur.com/xsLDn95.png" align= "center" height="80%" width="80%"/>

To better visualize this data you can also add an integrated chart from this data using PivotChart: 

<img src="https://i.imgur.com/t0weIF1.png" align= "center" height="80%" width="80%"/>

#### 2. Vlookup
Now, before stepping into advanced formulas, let's get to know, Vlookup.

This is one of the most used formulas in excel, it helps us find a certain value in one column and return a corresponding value from another column in the same row

Basicaly it's like a **"search bar"** for your **data**. Let's see how this works.

The equation itself will look like this:

**=VLOOKUP(lookup_value, table_array, col_index_num, range_lookup)**

Okay, now let's apply that equation to the spreadsheet, the first thing you gotta do is make a new column for the value you want to find, and on the next column your gonna input the equation.

<img src="https://i.imgur.com/EJSqODA.png" align= "center" height="80%" width="80%"/>
<img src="https://i.imgur.com/djnNHTZ.png" align= "center" height="80%" width="80%"/>

These images above shows how Vlookup can search how much really does each customer spend in your store. 

Pay attention to the formula, the **lookup_value** corresponds to the value you want to find (the "search bar"), while **table_array**  corresponds to the range of the cells you want to search, **col_index_num** is the column number for the value you want to return (in this case the final price), lastly there's the **range_lookup**, it contains two categories, **TRUE** (to find the approx. value) and **FALSE** (to find the exact value).

As you can see, **K2** acts as the **"search bar"** you can type whatever name on the data and it will return the price value on the next column, let's search for Kevin Hurst, manually from the data you can find how much Kevin spends at **A22**, now by using Vlookup you can easily search for Kevin's spending:

<img src="https://i.imgur.com/cQhWqMR.jpeg" align= "center" height="80%" width="80%"/>
<img src="https://i.imgur.com/2egYrdm.png" align= "center" height="80%" width="80%"/>
