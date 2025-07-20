# Brazilian E-Commerce Analytics (DuckDB SQL)

End-to-end analysis of Olist's e-commerce data using DuckDB SQL to derive actionable business insights.

## Key Findings

### 1. Revenue & Growth Trends
- **Monthly Revenue Surge**: Revenue grew from R$134.97 (Sep 2016) to R$994,849.49 (Nov 2017)
  
  <img width="624" height="401" alt="1 1" src="https://github.com/user-attachments/assets/5fb1851e-6860-470d-aa98-b9c5108adb37" />

- **YoY Growth**: 99% revenue increase between Jan-Sep 2017 and Jan-Sep 2018

  <img width="854" height="826" alt="1 2" src="https://github.com/user-attachments/assets/6506350b-7412-4eab-95c9-d63357796341" />

- **AOV Stability**: Average Order Value fluctuated between R$125-R$160, indicating growth is volume-driven
<img width="654" height="841" alt="1 3" src="https://github.com/user-attachments/assets/136ec57b-6468-4018-9e16-46a926092f1d" />



### 2. Product Category Performance
#### Top Revenue Drivers:
1. **Beleza & Saúde** (Health/Beauty) - R$1.26M 
2. **Relógios & Presentes** (Watches/Gifts) - R$1.21M
3. **Cama/Mesa/Banho** (Bed/Bath) - R$1.04M

<img width="1100" height="778" alt="2 1" src="https://github.com/user-attachments/assets/801774b0-8078-46ab-808b-27437916052d" />

   

#### Fastest Growing Categories (YoY):
1. **Portáteis Casa/Formo e Café** +5,572% 
2. **Construção/Ferramentas Iluminação** +3,043%
3. **Construção/Ferramentas Construção** +2,430%
    <img width="975" height="820" alt="2 2" src="https://github.com/user-attachments/assets/61b7ddb1-aa14-4ed1-a9fc-9e3f10deb741" />

   <img width="645" height="294" alt="2 2_r" src="https://github.com/user-attachments/assets/79f74eb6-3e86-48bb-b06c-597364917f8c" />


#### Premium Niches (High AOV):
- **PCs**: R$1,098 avg price/item (203 units sold)
- **Eletrodomésticos**: R$476 avg price/item

  <img width="645" height="294" alt="2 2_r" src="https://github.com/user-attachments/assets/858c8bbe-b39c-43a2-829f-3c521b1d049a" />


### 3. Geographic Insights
#### Top Revenue Cities:
1. Rio de Janeiro - R$278.3M
2. São Paulo - R$145.5M  
3. Belo Horizonte - R$96.3M

   <img width="222" height="272" alt="3 1_r" src="https://github.com/user-attachments/assets/673842bc-a411-44c2-8c00-f4f6b922793c" />


#### Delivery Bottlenecks:
- Slowest cities average **60-148 delivery days** vs national avg of ~15 days
<img width="700" height="778" alt="3 2" src="https://github.com/user-attachments/assets/86d10b87-7fa7-460f-8c12-02b0b57a4525" />


#### Revenue Concentration:
- Rio buyers spend **3× national average** per order
- São Paulo has high order volume but lower margins
<img width="700" height="778" alt="3 2" src="https://github.com/user-attachments/assets/2f28d613-f816-4e98-b7c7-67d09c8a8a44" />
<img width="700" height="778" alt="3 2" src="https://github.com/user-attachments/assets/39bbefaa-5298-4a8e-bacc-5371d1e076ae" />


### Business Impact
- Inventory Strategy: Double down on fast-growing home appliance categories
- Logistics Optimization: Prioritize delivery improvements in interior cities
- Pricing Strategy: Leverage premium category insights for upsell campaigns
- Marketing Focus: Allocate budget to high-value Rio de Janeiro market

### Data Sources
[Brazilian E-Commerce Dataset on Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

All analysis performed on Olist's public dataset:
- orders (99,441 rows)
- order_items (112,650 rows)
- products (32,951 rows)
- customers/geolocation (99,441/1,000,163 rows)



### setup tips:
- Download all CSV files from Kaggle (9)
- Create a new folder in your desktop
- Create a subfolder called data and put the 9 CSVs in it.
- Install DuckDB in CLI (terminal), see how to below
- Then in CLI run "duckdb brazil_ecom.db -ui"
- DuckDB UI should then open in a browser (the name brazil_ecom isn't mandatory, choose the name you want)

### Files
- `brazil_ecom.db` — the DuckDB file you can open with `duckdb brazil_ecom.db --ui`
- `data/` — contains the raw CSV files from Kaggle
- `notebooks/` — (optional) SQL code in notebook format

### Code
You'll find all the SQL code in the 'ecommerce_analysis.sql' file in this repository

### How to use
1. Install DuckDB via Homebrew: `brew install duckdb`
2. Run: `duckdb brazil_ecom.db --ui`
3. Start querying!


