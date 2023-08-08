# Exploratory Data Analysis on Supermarket Sales Dataset

## Introduction
The 'Supermarket Sales' dataset, available on Kaggle, contains transactional data from three supermarkets, encompassing 1000 records and 17 attributes. The attributes include 'Invoice id,' 'Branch,' 'City,' 'Customer type,' 'Gender,' 'Product line,' 'Unit price,' 'Quantity,' 'Tax 5%,' 'Total,' 'Date,' 'Time,' 'Payment,' 'COGS,' 'Gross margin percentage,' 'Gross income,' and 'Rating' (refer to Table 1).

## Table 1: Summary of Attributes
| Attribute                | Description                                              |
|--------------------------|----------------------------------------------------------|
| Invoice id               | Computer-generated sales slip invoice identification number |
| Branch                   | Three branches available (A, B, C)                      |
| City                     | Location of supercenters                                |
| Customer type            | Type of customers: Members (with member card) and Normal (without member card) |
| Gender                   | Gender type of customer                                 |
| Product line             | General item categorization groups (e.g., Electronic accessories, Fashion accessories, Food and beverages) |
| Unit price               | Price of each product in $                              |
| Quantity                 | Number of products purchased by customer                |
| Tax 5%                   | 5% tax fee for customer purchases                      |
| Total                    | Total price including tax                               |
| Date                     | Date of purchase (January 2019 to March 2019)           |
| Time                     | Purchase time (10am to 9pm)                             |
| Payment                  | Payment method used by customer (Cash, Credit card, Ewallet) |
| COGS                     | Cost of goods sold                                      |
| Gross margin percentage  | Gross margin percentage                                 |
| Gross income             | Gross income                                            |
| Rating                   | Customer stratification rating (Scale: 1 to 10)         |

## Data Cleaning
The data cleaning process involved the following steps:
1. Imported essential packages: pandas, seaborn, and matplotlib.pyplot.
2. Read the dataset using the read_csv() function.
3. Previewed the initial data rows using the head() function.
4. Gathered dataset summary information using the info() function.
5. Explored numeric data characteristics using the describe() function.
6. Checked the number of unique values in 'Invoice ID' and 'gross margin percentage' columns using nunique().
7. Removed irrelevant 'Invoice ID' and 'gross margin percentage' columns using drop() function.
8. Converted 'Date' and 'Time' columns to datetime format using to_datetime().
9. Segregated data into two dataframes: one for numerical data and one for categorical data.
10. Created histograms to visualize numeric column distributions.
11. Employed bar plots to visualize categorical column distributions.
12. Eliminated the 'Branch' column as 'City' provided more informative insights.
13. Checked for duplicate rows using duplicated() function, confirming no duplicated data.

## Missing Data
The 'Supermarket Sales' dataset exhibited no missing data, obviating the need for imputation or column removal.

## Data Stories and Visualizations
Prior to delving into comparative visualizations and narratives, histograms (numerical) and countplots (categorical) were generated for the 13 variables within the dataset.

### Numerical Variables – Histograms
- Transaction total count reveals a declining trend as transaction total decreases.
![numerical plot; total](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/7b2be5de-6149-4995-84dd-3bc11ed6b1b3)
- Uniform distribution for tax, COGS, and gross income due to constant tax and gross margin percentage.
![numerical plot; tax](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/2d147fe7-52df-4cc2-b5e6-22e680dfe193)
![numerical plot; cogs](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/0da929b3-7554-4501-ae20-177d34361f3e)
![numerical plot; gross income](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/bac26b61-c468-4980-9d09-eb92e7e19aef)
- The rating scores are between 4 and 10. The scores that are given most frequently appear to be between 6 and 7, and the lowest scores most frequently given are between 5 and 6.
![numerical plot; rating](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/1ca0e340-6f2a-404d-ac7e-c4ff096960cb)
- Quantity per invoice frequently ranges from 1 to 10 items.
![numerical plot; quantity](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/6e093547-4ba5-4078-9635-4dcc763818b1)
- Unit price distribution spans from $10 to under $100.
![numerical plot; price](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/22ab45c6-970d-4549-9349-e3a407427089)


### Categorical Variables – Countplots
#### Payment
![categorical plot; payment](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/f1423b46-fd97-4ab6-9155-420a63b5d2b3)
| Payment Method   | Count |
|------------------|-------|
| Ewallet          | 345   |
| Cash payment     | 344   |
| Credit card      | 311   |

#### Customer Type
![categorical plot; customer](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/c606fab7-7287-41cd-a239-0f5b4e38b4f6)
| Customer Type | Count |
|---------------|-------|
| Member        | 501   |
| Normal        | 499   |

#### Gender
![categorical plot; gender](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/7b3ccd2e-e99e-4e10-967f-423e3cd0fc92)
| Gender | Count |
|--------|-------|
| Male   | 499   |
| Female | 501   |

#### City
![categorical plot; city](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/3039da1e-9fbd-44d7-b37b-4d6059f2ca8c)
| City       | Count |
|------------|-------|
| Yangon     | 340   |
| Mandalay   | 332   |
| Naypyitaw  | 328   |

#### Product Line
![categorical plot; product line](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/b53ea391-e17c-4201-b4bc-4ab76324fc9e)
| Product Line         | Count |
|----------------------|-------|
| Fashion accessories  | 178   |
| Food and beverages   | 174   |
| Electronic accessories | 170 |
| Sports and travel    | 166   |
| Home and lifestyle   | 160   |
| Health and beauty    | 152   |

### Comparative Visualizations
1. Exploring numerical variables - Correlation Heatmap:
The highest correlation (=0.71) is between the quantity sold and the gross income (in turn, thus also the total, cogs, and tax 5%).
 A high quantity of items sold is positively correlated with a high gross income. This is very logical as more items purchased
(i.e., a higher quality will equal a higher total and, in turn, a higher profit/gross income). Similarly, the second-highest positive correlation is
 between unit price and gross income (=0.63), which again makes sense as more expensive items will naturally lead to more expensive invoice totals and,
in turn, higher gross incomes. All the other numerical variables have correlations very close to 0, whether they are + values or – values.
This means that these comparisons are not highly correlated at all. There is therefore not much of a relationship between the variables that meet at blue squares.
For example, there is not much of a relationship between customer ratings and gross income.
![correlation heatmap](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/e07a0441-8a74-4ce6-a11b-54b9df67527a)


2. Exploring categorical variables - Product lines and City:
Using grouped bar plots, we can see the distribution of the numerical variables in relation to the city
(and branch A = Yangon, branch B = Naypyitaw, Branch C = Mandalay) and product lines.
![quantity by city and product](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/f44f3fa0-d92b-4a49-9de1-752881bd082f)
![gross income by city and product](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/d0462757-94e7-41a2-9ca2-a5d2f5c9d8eb)
![rating by city and product](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/25fdc113-ca10-4dfd-9e91-0903573127e9)
![price by city and product](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/13966687-3e23-4b0c-a83e-7807676d32d3)

Above are the outputs for the averages of all categorical variables of the invoices based on the city of purchase and the product line it falls under.
In general, there are no apparent outliers (top or bottom) for either of the numerical variables in terms of the city or product line. However, the displayed graphs
provide a good overview for all branches to compare their average income, quantities sold, customer ratings, and units per product line, but also to compare with 
the other branches.
*Similar averaged grouped barplots could be made for all categorical variables, such as payment method and gender, customer type and gender, or any other
combination.

3. Exploring the main dependent variable – Sales:
Above is one graph looking at the average gross income per city and product line, but the sales aspect is arguably the most looked at or important dependent variable.
Although the costs of goods sold differ per product, the gross margin percentage for all products in all lines and cities are the same. This eases the visualization
and factors that have to be considered when exploring.
![income distribution by product line](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/54061598-333e-47df-ba5c-c5dc8f2bf527)

The graph above is a boxplot of the gross income distribution over all the product lines. From this it is clear that the distribution of sales (gross income) is quite 
similar across all product lines. There are outliers above the maximums for Sports and travel, Food and beverages; and fashion accessories.
The graph above is a boxplot of the gross income distribution over all product lines. From this, it is clear that the distribution of sales (gross income) is quite similar
across all product lines. There are outliers above the maximums for Sports and Travel, Food and Beverages, and Fashion Accessories.
![image](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/7e8d79c0-f0b9-40eb-b963-c5eebfa23769)

For completion, above is also a barplot of the total gross income per product line, which similarly to the boxplot shows little difference between product lines.
Food and Beverages have the highest total gross income, while Health and Beauty have the lowest.
![image](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/0bae3ec3-af6a-4d6a-92d3-9ed41baf64bc)

From this pie chart, we can see that the payment methods are close to equally responsible for the total amount of income the supermarkets generate. 
Cash is responsible for the most income, with 34.7% of sales stemming from this payment method.
![image](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/44e6e903-0de3-41b5-9de6-5dc762fe7aeb)

This stacked barplot shows member customer vs normal customer total income split by female and male. From this, we can see that the member customers are responsible 
for slightly more of the gross income. Similarly, there are also slightly more female members compared to male members.
![image](https://github.com/LizeMireille/Exploratory-Data-Analysis-on-Supermarket-Sales-Dataset-/assets/127414934/87a202ae-7140-4ba3-b82c-636149533836)

his lineplot shows the total gross income per day for the recorded period (01 Jan 2019 - 01 April 2019). This graph gives a general overview of the gross income per day 
over the four-month period. We can deduce that the total income fluctuates between an estimated $50 and $350. We can also deduce that it fluctuates a lot and changes quite
drastically between the $50 and $350 margin. Looking at the value counts, we can see the highest total gross income in a day for the period was $355,907 on 2019-03-09. 
The lowest total gross income in a day for the period was $44,487.5 on 2019-02-13.

## Aspects for Improvement:
This EDA did not look at the time variable. A graph can be added to look at, for example, the average gross income per hour of the day. 
Similarly, this EDA looked at gross income (to represent the sales/income of the supermarket) as the main dependent variable, but any of the other variables could also 
be focused on. Lastly, this EDA only looks at visual representations to comment on distributions of the data. No statistical testing or analysis was added in this EDA.
