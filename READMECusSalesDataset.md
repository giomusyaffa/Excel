# Step-by-step Analysis of Customer Sales Dataset 🖥️
## Overview 📘
This project analyzes customer sales data to uncover key trends, product performance, and customer behavior. The goal is to transform raw transactional data into actionable insights using Microsoft Excel’s **advanced formulas**, **Pivot Tables**, and **data visualization tools**.
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

To seperate it into each collumns, all you have to do is convert text to columns in the **Data** menu and choose delimeted, with *comma* as the delimiters (since the values are seperated by a comma):

<img src="https://i.imgur.com/V0tu9AR.png" align= "center" height="80%" width="80%"/>

Finally you have your readable, ready-to-analyze data:

<img src="https://i.imgur.com/nQbfdjy.png" align= "center" height="80%" width="80%"/>

### Step 2
#### Pivot Tables
Now, the easiest way to interpret and analyze large amounts of data without using any complicated functions is by using this interactive tool.

By using **pivot tables** we can choose specific fields from our data and categorize it to each respective columns and values

Let's say you want to know if by discounting a product will boost sales, you can do that by selecting **product category** and **discount applied** to the rows and **quantity** to the values.

<img src="https://i.imgur.com/UA5YEH4.png" align= "center" height="80%" width="80%"/>

As you can see from the pivot table above, a boost of sales after applying discount only happens to **books**, and **electronics** while **groceries** are unaffected and **clothing** shows a **decline** in sales.
