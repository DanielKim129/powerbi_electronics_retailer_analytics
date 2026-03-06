# Project Background
Boost Digital is a global electronics retailer that sells a wide variety of electronic goods both online and in store across 8 countries. It was established in 2010 and has since then expanded globally over time. This report aims to provide insights through analysis of the company's data from FY2017 to FY2021 year-to-date assuming that the company is currently in FY2021. Note that this company's fiscal year runs from 1 July to 30 June, in line with the Australian financial year.

The project involved developing a Power BI report for the company in order to synthesise and analyse its vast amounts of data from FY2017 to FY2021 and better understand key trends and drivers within sales and profit.

My interactive Power BI report that I built and designed can be found [here](https://app.powerbi.com/view?r=eyJrIjoiOWQ3MDBkZDMtMDljYS00NWU4LTg3YzYtNGM0ODJhYmIzN2RiIiwidCI6IjY2NTI4MjVkLTE2YjMtNDUwOC1iYjM2LWU5ODYxNTA2ZGM5MyJ9&embedImagePlaceholder=true). I have also attached screenshots from this Power BI report to accompany relevant analysis throughout this readme.

Insights and recommendations from the analysis are provided in the following areas:

- **Key Trends:** An evaluation of historical patterns of key metrics over time including net sales, average delivery days and gross margin.
- **Product Performance:** An assessment on the performance of various products and their contribution to gross profit and sales, along with root-cause analysis for areas of key concern. 
- **Store Region Performance:** A deep dive into the relationship between store region and gross profit.

# Data Structure & Initial Checks

The main database structure for Boost Digital follows a star schema that is comprised of five tables as shown below: Fact_Sales, Dim_Date, Dim_Products, Dim_Stores and Dim_Customers with a total row count of 79,500 records.

<img width="1471" height="1199" alt="ER Diagram Boost Digital" src="https://github.com/user-attachments/assets/3fcce726-1c2f-41f7-a410-481670fc2816" />

The original dataset was sourced from [Maven Analytics Free Datasets](https://mavenanalytics.io/data-playground/global-electronics-retailer), but for reproducibility, I have included the version I used directly in this repository in case the source is updated. Data cleaning was performed on this data by removing unused columns, renaming columns and replacing error-prone values. Afterwards, data modelling was performed by establishing relationships and creating a star schema as above with the inclusion of a new date table.

# Executive Summary

### Overview of Findings

From FY2017 to FY2021, the company exhibited strong annual seasonal patterns in net sales which tended to hit a trough in April of each year before rising again to peak in between December and February the following year. The company experienced negative YoY growth in FY2021 (YTD) for key performance indicators including -75.88% YoY growth for net profit, -75.82% for gross profit and -76.28% for units sold. This decline could largely be attributed to the pandemic that began to take effect from early 2020. Further, the Games and Toys category has consistently underperformed since FY2017 with boxed games of this category showing concerningly low gross profit. Finally, despite above average gross profits in Italy, it currently has the least number of stores in operation.

<img width="1122" height="628" alt="Overview page" src="https://github.com/user-attachments/assets/3611faf8-6353-4128-a0b4-ee32678be0ee" />

Overview Page

# Insights Deep Dive
### Key Trends:

* The company's net sales follow a strong seasonal pattern where sales tend to fall until May each year before sharply increasing again. However, in the fiscal year of 2021 (YTD), the company's YoY growth for net sales fell to an all-time low in five years of -75.88%. This decline reflects the decline in consumption and rise in lock-downs after the pandemic became an international concern from January 2020.

<img width="718" height="238" alt="Category_1_Insight1" src="https://github.com/user-attachments/assets/9eda4a50-a4eb-43ff-84f4-982c588f4f40" />

Net Sales Over Time (FY2017-FY2021 YTD)

* Pre-pandemic trends show that the company experienced positive YoY growth over time in net sales, gross profit and the total number of orders. In turn, these metrics peaked in December 2019 with gross profit reaching $1,435,548.24. Such positive YoY growth highlights that the company was doing well and growing before the external shock of the pandemic.
  
* The average number of days to deliver continued to decrease from FY2017 to FY2021 at a decreasing rate. The company's YoY growth (YTD) of average delivery days for FY2021 vs FY2020 was -2.97%. The fall in delivery days is a testament to the company's rise in efficiency with handing delivery.

* Despite periods of stable growth and sharp decline, the company's gross margin remained relatively indifferent to these periods as it rather showed a roughly stationary trend. For example, when other metrics showed decline due to the effects of the pandemic, gross margin increased 0.15% in FY2021 vs FY2020 on a YTD basis. This difference about the gross margin reflects that the company did not make any significant adjustments to the profitability of producing its products in response to the environment.

<img width="302" height="172" alt="category_1_Insight4" src="https://github.com/user-attachments/assets/85ee0e28-034c-42e7-ae3e-915d7fa2a53d" />

### Product Performance

* Computers consistently remained the top product category from FY2017 to FY2021. In the current fiscal year of 2021 (YTD), computers account for 48.26% of gross profit. Further, overall product positioning based on the data aggregated from FY2017 to FY2021 (YTD) shows that the computers category was an outlier by performing substantially better compared to the rest of the categories. Computers also followed an increasing trend in net sales over time before the pandemic-induced decline in 2020.

<img width="472" height="291" alt="Category_2_Insight_1" src="https://github.com/user-attachments/assets/e98d9535-e0d2-4e3f-b801-5672bbcfa58e" />

Overall Product Positioning (FY2017-FY2021)
Note: The blue dashed line represents the median
  
* The Games and Toys category has continued to underperform the most since FY2017 as shown above. In FY2021 YTD, the category's gross margin is below the median of 58.32% by sitting at 54.65%, as does net sales which sits at $51,229.39 when the median is $344,471.71. This underperformance is due to the low sales or relative popularity of both Download Games and Boxed Games despite being sold for less profit (low gross margin). Boxed Games have consistently generated the least amount of gross profit among all the company's products from FY2017 to FY2021 (YTD) as Boxed Games generated a total gross profit of $49,999.16, which was about 95.11% below the median.
  
* The home appliances category started to decline in performance from FY2020 with YoY Growth of -26.01% for gross profit, -28.14% for total orders and -0.16% for gross margin in FY2020. This decline became first apparent from the first quarter of FY2020 before the pandemic. As a result of this decline, the home appliances category did not show an increasing trend in gross profit before the pandemic as opposed to the other categories, which means the decline in home appliances should not simply be attributed to the pandemic.

<img width="575" height="227" alt="Category_2_Insight3" src="https://github.com/user-attachments/assets/06d0e4d2-69af-4e76-a790-f66f2a236e14" />

Gross Profit from Home Appliances (FY2017-FY2021 YTD)

* Deeper analysis for the root cause of this decline in the home appliances category has shown that all of its subcategories exhibited the pre-pandemic decline with concerningly large negative YoY growth in gross profit (FY2020) as opposed to other categories. Among these subcategories under home appliances, the subcategory of microwaves displayed the worst YoY growth of -46.13%. This decline was not unique to a specific brand but was present in all brands of this microwave subcategory.

<img width="352" height="448" alt="Category_2_Insight_4" src="https://github.com/user-attachments/assets/205fa843-3f27-4784-a441-f994faebe48c" />

Data Filtered to Microwaves (FY2020)

### Store Region Performance:

* Stores in France consistently generated the least amount of gross profit from FY2017 up to FY2020 but in FY2021, they generated more gross profit than Netherlands and Italy. Upon further examination France's gross profit experienced a smaller decline, its YoY growth (FY2021 YTD) being -65.68%, than Italy with -86.87% and Netherlands with -78.79%. Hence, this change in ranking could be attributed to Boost Digital's electronics stores in France being potentially less impacted by the pandemic than those of Netherlands and Italy. 
  
* Stores in the United States have been the greatest contributor of gross profit since FY2017, even more than the company's online store that includes all transactions online regardless of the customer's country. From FY2020 up to FY2021 YTD (in most recent years), gross profit in the US more than doubled that of online transactions. In the same period, average gross profit per physical store in the US was $257,097.87 which was about 68.29 % greater than the average of $158,716.67 (the online store and all stores that were not in operation during these years were excluded).

<img width="351" height="442" alt="Category_3_Insight_2" src="https://github.com/user-attachments/assets/5fb0c2ff-edda-47b8-a585-3b598bc7f3c4" />

Data Filtered to the US (FY2020-FY2021 YTD)

* Italy was shown as the third worst country for total gross profit between FY2020 and FY2021 (YTD). However, deeper analysis revealed that the average gross profit per store in Italy was $172,655.12, which was above average. The underlying cause for the low level of aggregate gross profit was attributed to Italy only having two stores in operation between FY2020 and FY2021 (YTD).

<img width="359" height="188" alt="Category_3_Insight3" src="https://github.com/user-attachments/assets/c9a9281c-ae74-4a7a-86ca-7fc147a9d871" />
Gross Profit from Italy (FY2020-FY2021 YTD)

# Recommendations:

Based on the insights and findings above, the following recommendations are provided:

* The subcategory of boxed games consistently generated the least amount of gross profit from FY2017 to FY2021 (YTD) and in total, gross profit from this subcategory was 95.11% below the median. The company should consider replacing the current brands of Tailspin Toys and Southridge Video in the subcategory of boxed games or discontinuing the subcategory entirely as it is not profitable for the company and resources can be allocated better elsewhere.
  
* The company may consider adding newer and more modern technologies to the home appliances category in order to address its pre-pandemic decline (YoY gross profit growth of -26.01% in FY2020) and loss in popularity. Currently, the products in this category are limited to the more traditional types of products such as fans and microwaves. Adding newer and trending technologies such as air fryers to the home appliances category may significantly help it to recover from the pre-pandemic decline.
  
* Given that average gross profit in the US is 68.29% above overall average (FY2020-FY2021 (YTD)), the company may consider engaging the US market more to maintain popularity and customer loyalty for example with news, subscriptions and deals. 
  
* Gross profit from Italy is above average yet there are only two stores in operation. Being in such a situation may mean wasting potential opportunities to leverage on the company's popularity in Italy. The company should consider expanding by opening up new stores in Italy.
