# 🏠 Housing Market & Real Estate Analysis — Power BI Dashboard

A multi-page Power BI report analysing residential real estate sales performance across regions, property types, and time periods. Built to surface pricing trends, YOY sales growth, and the relationship between offer and purchase prices at a regional and property-type level.

---


| Page | Description |
|------|-------------|
https://github.com/marwaanaarif-gif/Housing-market-overview-power-bi/blob/main/housing%20market%20overview.png | House Market Overview |
https://github.com/marwaanaarif-gif/Housing-market-overview-power-bi/blob/main/Sales%20overview.png | Sales Overview |
https://github.com/marwaanaarif-gif/Housing-market-overview-power-bi/blob/main/house%20type%20overview.png| House Type Overview |

---

## 📄 Project overview

### ❔ Problem statement
Real estate markets shift quickly — prices move by region, property type, and macroeconomic conditions like interest and inflation rates. 
This dashboard was built to answer a core question: **where are prices moving, which property types are driving volume, and how closely are offer prices tracking final purchase prices?**

### 🛠️ What I built
A 3-page interactive Power BI report covering:
- Market-level KPIs (units sold, 12-month revenue)
- Regional sales and price-per-sqm breakdowns
- YOY sales growth trends by house type
- Offer vs. purchase price comparison (scatter analysis)
- Key driver analysis: what factors most influence purchase price
- Cross-filtering slicers by Area, City, Sales Type, and Region

---

## 🗂️ Report pages

### Page 1 — House Market Overview 🛋️
High-level market snapshot with top-line KPIs and pricing trend visuals.

| Visual | Type | Key fields |
|--------|------|-----------|
| YOY sales growth by house type | Line chart | `YOY_sales_growth`, `SALES_TYPE` |
| Offer price vs. purchase price | Scatter chart | `OFFER_PRICE`, `PURCHASE_PRICE` |
| Median price by region | Bar chart | `MEDIAN PRICE`, `REGION` |
| Units sold (latest quarter) | KPI card | `Total_Units_Latest_Quarter` |
| 12-month revenue | KPI card | `LAST12_REVENUE` |

### Page 2 — Sales Overview 📈
Regional and time-based sales performance with key driver analysis.

| Visual | Type | Key fields |
|--------|------|-----------|
| Sales per region | Bar chart | `Sales per region` (measure), `REGION` |
| YTD sales table | Matrix | `TOTAL YTD` (measure), Year / Quarter / Month |
| Average sale price per SQM by region | Donut chart | `AVERAGE SALEPRICE per SQM`, `REGION` |
| Key drivers of purchase price | Key influencers | `PURCHASE_PRICE`, `AGE` |
| Offer per SQM ratio by sales type | Bar chart | `OFFER PER SQM RATIO`, `SALES_TYPE` |

### Page 3 — House Type Overview 🗃️ 
Deep dive into how property characteristics (type, size, age) interact with price.

| Visual | Type | Key fields |
|--------|------|-----------|
| Avg offer vs. purchase price by house type | Clustered bar | `HOUSE_TYPE`, `PURCHASE_PRICE`, `OFFER_PRICE` |
| Avg interest & inflation rate by house type | Clustered bar | `HOUSE_TYPE`, `NOM_INTEREST_RATE%`, `DK_ANN_INFL_RATE%` |
| Avg SQM and SQM price by house type | Combo chart | `HOUSE_TYPE`, `SQM`, `SQM_PRICE` |
| Slicers | Filters | `AREA`, `CITY`, `SALES_TYPE`, `REGION` |

---

## 👷🏾 DAX measures

Custom measures built in the `MEASURE TABLE`:

| Measure | Logic summary |
|---------|---------------|
| `Sales per region` | Total sales value aggregated by region |
| `TOTAL YTD` | Year-to-date cumulative sales using a time intelligence filter |
| `AVERAGE SALEPRICE per SQM` | Average of `PURCHASE_PRICE / SQM` across filtered context |
| `OFFER PER SQM RATIO` | Average offer price relative to SQM — used to compare market aggressiveness by sales type |

---

## 🪪 Data fields

| Field | Description |
|-------|-------------|
| `PURCHASE_PRICE` | Final transaction price |
| `OFFER_PRICE` | Initial listed/offer price |
| `REGION` | Geographic region |
| `AREA` | Sub-region area |
| `CITY` | City of property |
| `HOUSE_TYPE` | Property type (e.g. detached, apartment, townhouse) |
| `SALES_TYPE` | Transaction type (e.g. market sale, auction) |
| `SQM` | Property size in square metres |
| `SQM_PRICE` | Price per square metre |
| `AGE` | Property age at time of sale |
| `DATE` | Transaction date (with Year / Quarter / Month hierarchy) |
| `YOY_sales_growth` | Year-over-year % change in sales volume |
| `NOM_INTEREST_RATE%` | Nominal interest rate at time of sale |
| `DK_ANN_INFL_RATE%` | Danish annual inflation rate at time of sale |
| `Total_Units_Latest_Quarter` | Units sold in the most recent quarter in the dataset |
| `LAST12_REVENUE` | Rolling 12-month revenue |

---

## 🔍 Key findings

- **Offer-to-purchase alignment**: The scatter chart on Page 1 shows how closely offer prices track final sale prices — Lower priced houses shows variences between the prices but as the value of houses go up it                                     prices tend to remain the same .
- **Regional price spread**: The median price bar chart reveals significant variation across regions — Jutland commands the highest median, while Bornholm sits considerably below market average.
- **YOY trend**: Sales growth by house type on the line chart shows houses on auction experienced the sharpest YOY movement.
- **SQM price driver**: Larger properties don't always yield lower per-SQM prices — the combo chart on Page 3 shows sqm prices of farms are much lower when compared to those of apartments even though the sqm of                          the former are much bigger in value 
- **Key influencer**: The key drivers visual (Page 2) identifies property age as a notable factor in purchase price variation.

---

## 💻 Tools used

- **Power BI Desktop** — report authoring, data modelling, DAX
- **DAX** — custom measures (YTD, per-SQM ratios, regional aggregates)
- **Power Query** — data transformation and column preparation
- **MS Excel** — data cleaning 

---

## How to open

1. Download [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
2. Clone or download this repository
3. Open `Housing market overview (real estate project).pbix`
4. Use the slicers on Page 3 (Area, City, Sales Type, Region) to filter across all visuals

---


