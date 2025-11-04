# Step-by-step Analysis of A Customer Sales Dataset 🖥️
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
#### **Convert the .csv file**
The first step in analyzing a data, especially when acquiring it from an open source data like **Kaggle** is to convert it into Excel.

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

Pay attention to the formula, the **lookup_value** corresponds to the value you want to find (the **"search bar"**), while **table_array**  corresponds to the range of the cells you want to search, **col_index_num** is the column number for the value you want to return (in this case the final price), lastly there's the **range_lookup**, it contains two categories, **TRUE** (to find the approx. value) and **FALSE** (to find the exact value).

As you can see, **K2** acts as the **"search bar"** you can type whatever name on the data and it will return the price value on the next column, let's search for Kevin Hurst, manually from the data you can find how much Kevin spends at **A22**, now by using Vlookup you can easily search for Kevin's spending:

<img src="https://i.imgur.com/cQhWqMR.jpeg" align= "center" height="80%" width="80%"/>
<img src="https://i.imgur.com/2egYrdm.png" align= "center" height="80%" width="80%"/>

#### 3. IF Function and The Derivatives
Diving into a more complex formula, are Nested-IF's, the function itself basically returns one value if a condition is true and another value if it's false. 

There are some couple variations of IF's function you can apply to the spreadsheet to make your desireable output, one of those are combining IF's with; AND; OR; and even IF's itself. Let's see some examples:

Starting from the basics, by using

**=IF(logical_test, value_if_true, value_if_false)**

We can track multiple purchase of a product (more than 5 items) on a single transaction

<img src="https://i.imgur.com/ZuLFT8P.png" align= "center" height="80%" width="80%"/>
<img src="https://i.imgur.com/JtY5LyL.png" align= "center" height="80%" width="80%"/>

As you can see from the picture above we can easily do it by using IF function, with purchases over 5 items are flagged as **Yes**.

Let's do another one, this time we integrate AND to the function, with the formula:

**=IF(AND([logical1],[logical2],...); value_if_true; value_if_false)**

For example, what if we want to mark if a purchase is made during a weekend AND had a discount, it's going to look like this:

<img src="https://i.imgur.com/tPmETNp.png" align= "center" height="80%" width="80%"/>
<img src="https://i.imgur.com/tIOb73j.png" align= "center" height="80%" width="80%"/>

By combining **IF** with **AND** function we can easily label the purchase that check both the conditions, as shown from the picture above.

Another application of IF function is **Nested-IF**, it's where an if statement is placed inside another if statement to test multiple, dependent conditions. 

Next, we have **IFs** function, which basically is the same as **IF** function just with more conditions, such as this customer tiering; 
- **Platinum** associated with customers with purchases over 8 items
- **Gold** associated with customers with purchases over 5 items
- **Silver** associated with customers with purchases over 2 items
- **Bronze** associated with customers with purchases only 1 item.

Which will look like this:

<img src="https://i.imgur.com/12dginw.png" align= "center" height="80%" width="80%"/>
<img src="https://i.imgur.com/r7C0rX2.png" align= "center" height="80%" width="80%"/>

Another application of IF function is **Nested-IF**, it's where an if statement is placed inside another if statement to test multiple, dependent conditions. 

This can be used in the spreadsheet to make a sales performance indicator, with sale over 300 are **High**, over 100 are **Medium** and less than 100 are **low**:

<img src="https://i.imgur.com/JU9G4O8.png" align= "center" height="80%" width="80%"/>
<img src="https://i.imgur.com/Zoaclq5.png" align= "center" height="80%" width="80%"/>


### Step 3
#### Power BI
Now, let's start visualizing the data. Using this
![Recording 2025-11-04 143154](https://github.com/user-attachments/assets/febc3521-7d9b-4d6c-98c4-331d1b33085e)
