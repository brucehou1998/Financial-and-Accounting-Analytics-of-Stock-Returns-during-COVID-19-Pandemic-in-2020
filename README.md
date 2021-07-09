# Financial-and-Accounting-Analytics-of-Stock-Returns-during-COVID-19-Pandemic-in-2020

In 2020, global pandemic generated a great economic recession. Stock market unprecedentedly plunged over 30% in mid-March, terrifying most of the investors. Yet surprisingly, full recovery prevailed right after several circuit brakes, regarded as an 'abnormal phenomenon' by some experts. Among stock market under pandemic, it is worth noting that overall return varies across companies as well as industries. Some stocks reached all-time high in the rest of the year while others still lagging behind S&P500. 

Difference of stock returns are mostly driven by actions from the one who own them, investors. Stockholders will purchase more if they are confident, and vice versa. Various issues may affect investors' confidence, though. Financial health of a company could be one of those. In this project, we strive to figure out how financial ratios in 2019 influence stock return in 2020 at the industry level. We measure financial data from fiscal year 2019 since it is the only visible report for investors in early 2020.

### Data Preparation

To prepare data for analysis, we collect business information across 2500+ companies in the US, including stock return in 2020, industry codes, and financial data, from Wharton Research Data Services (WRDS). We further simplify and prepare them. Stock return in 2020 are separated into two terms based on lowest stock point in March, from January to March and from April to December. First term captures devastating market loss while second term comprises miraculous recovery. 

For industry codes, we capture 4 types of classification methods, Standard Industrial Classification (SIC), North America Industry Classification (NAICS), GGROUP in Global Industry Classification Standard (GICS), and GSECTOR in GICS. For financial data, we drop columns whose missing value accounts for a high percentage. We keep remaining columns and drop their missing values by rows. Furthermore, we invert some of financial ratios to balance their distribution when calculating those ratios. After obtaining all necessary data, we merge them all together.

### Preliminary Analysis

First part of analysis mainly focuses on selecting the industry code that creates the best classifications of industries. We measure quality of classification based on three criteria: Adjusted r square from fixed effect, distribution of companies among each industry, and numbers of industry in total. Among 4 classification methods, GSECTOR in GICS outstrips others given highest adjust r-square from fixed effect in separating industries, the most balanced distribution of companies in each industry, and the most moderate numbers of industries in total. 

The next step is to deal with financial ratio. Among all financial variables we created, we select 10 variables due to their highest absolute correlation value with stock return. We then run two linear regressions: One measures relationship between early stock return and financial ratio; the other analyzes the late stock return. Financial variables that show statistically significance are selected for further analysis. 

In the regression, EBIT/Price, Book/Price, Retained Earnings/Price, Sales/Price, and Debt Ratio negatively correlates with stock return in early 2020. In late 2020, Earning/Price, Retained Earning/Total Assets, and EBIT/Total Assets are negatively correlated with stock return. However, Sales/Price, Asset Turnover Ratio, Cash/Total Assets, and Long-Term Debt/Total Assets are positively correlated.

Among all selected financial ratios, negative correlation of debt ratio with stock return in early 2020 makes economic sense as higher ratio reflects higher debt by assets, which is a bad sign for companies. In late 2020, positive correlation between stock return and 3 financial ratios (Cash/Total Assets, Sales/Total Assets, and Asset Turnover Ratio) is interpretable at the economic perspective since higher ratios stands for more cash, sales, and revenues per assets, which is beneficial for firms.

