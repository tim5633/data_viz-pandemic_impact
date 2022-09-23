# data_viz-pandemic_impact
## 1. Introduction
The attention revolves on the effects of the Covid-19 pandemic on businesses. We utilized `matplotlib`, `seaborn`, `plotly` package to present three plots.

## 2. Dataset
The data repository of Companies House provides [series of compressed folders](http://download.companieshouse.gov.uk/en_output.html) comprising firm-level attributes you may find useful. If you need more granular data please refer to [monthly files](http://download.companieshouse.gov.uk/en_monthlyaccountsdata.html).

## 3. Results of Plots

### Graph1: Company Created During Pandamic
![image](https://user-images.githubusercontent.com/61338647/192067014-62e0fa01-eff6-4adb-b400-1ae26c94cb40.png)

**Main insight:**
There are three waves of the impact of covid pandemic, which is 2020-03 to 2020-05, 2020- 10 to 2021-01, 2021-06 to 2021-10.
1. The Sensitivity Gap becomes smaller over time, meaning that gradually the motivation of establishing the company would not be influenced by pandemics, same as the trends in UK stock price and GDP.
2. The percentage of different industries of each stacked bar did not change over time, though there is some growth and falls with the covid cases trends.

**Design chose:**
1. We would use twinx to share the same x-axis of the time period, with the inverse y of covid cases, the reason for using inverse covid cases is that both y would share the same trends and could easily compare with each other.
2. The Sensitivity Gap is the key part of the graph to see with reduction of covid influences.
3. By inspecting into UK gov website, we further cut down the business classification in order not to have too many variables and useless information at the same time. From 0 to 19 to generalize different sectors. In order not to show too much text in the graph, we plotted out only with a number on it. The classification could be seen as below:
<img width="671" alt="Screenshot 2022-09-23 at 11 59 40 PM" src="https://user-images.githubusercontent.com/61338647/192067269-e180062d-d897-43cd-820f-80767f7fbefe.png">

### Graph2: Relationship of Mortgages outstanding and diversification
![image](https://user-images.githubusercontent.com/61338647/192067324-cd2c870f-cea5-4008-a890-c4e5420e1914.png)

**Main insight:**
We randomly extract 5% of the data during the covid impact periods to do the GLM model with Poisson family testing
<img width="684" alt="Screenshot 2022-09-24 at 12 01 07 AM" src="https://user-images.githubusercontent.com/61338647/192067393-b349b346-793c-46f1-8d81-503ac50ca87d.png">

1. The results showed the SIC sum counts will have a significant negative influence on the Outstanding Mortgages.
2. When the covid impact, a company with high diversification would spread the risk and be less likely to face financial distress.
3. Public Limited Companies have more fitted to the model, and Private ones usually sticks to low diversification but are less likely to outstand.

**Design chose:**
1. The upper graph shows the trend of low diversification with high Mortgages Outstanding. The bottom graph compares to different company category performance.
2. Node size represents diversification, bigger with more diversity.
3. If changing the color into IncorporationDate, we might see some trends related to
covid cases.


### Graph3: Indusrties clusters in London
<img width="1059" alt="Screenshot 2022-09-24 at 12 02 53 AM" src="https://user-images.githubusercontent.com/61338647/192067520-19114b0b-f588-43a9-9a26-6ffee9e91c32.png">
The Dynamic Graph3 is available HERE

[monthly files](http://download.companieshouse.gov.uk/en_monthlyaccountsdata.html).

**Main insight:**
1. There are two clusters in the graph of the region of Mayfair and the City of London. Separating per month, the clusters always stay in the same regions.
2. Wikipedia claims that the main industry in the City of London is Financial services, and Mayfair is well known for arts and galleries.
3. Indicating that with the same profession, the diversification of a company is less and the company would specialize in certain areas, presenting to the blue color in the Graph.
**Design chose:**
With the interactive plot, it is easy to see the fixed trend of industries staying at the specific area, combined with low SIC counts. We could see that London has a strong geographical distribution between different industries.










