## 🔎 Key Insights — Housing Market & Real Estate Analysis

This file documents the analytical findings from my Power BI dashboard.

---

## Page 1 — 📌 Market-level findings

### Offer vs. purchase price relationship
- **Visual**: Scatter chart, `OFFER_PRICE` vs. `PURCHASE_PRICE`
- **What to note**: Are properties generally selling above, below, or at asking? Is there a cluster of outliers? Which sales types show the widest spread?
- **Why it matters**: A tight cluster along the diagonal = efficient market pricing. Wide spread = negotiation room or distressed sales in the mix.

### YOY sales growth by type
- **Visual**: Line chart over time by `SALES_TYPE`
- **What to note**: Which property type peaked/dropped most sharply? Is growth recovering or still declining?

### Median price by region
- **Visual**: Bar chart
- **What to note**: Name the top and bottom regions. Percentage gap between highest and lowest.

---

## Page 2 — 📌 Sales performance findings

### Regional sales distribution
- **What to note**: Which region drives the most volume? Is high volume correlated with high price per SQM, or are they inversely related?

### Average sale price per SQM — donut chart
- **What to note**: Which region has the highest price density? Compare to the bar chart on Page 1 (median price) — does the same region rank highly in both metrics?

### Key influencer — what drives purchase price
- **Visual**: Key drivers visual using `PURCHASE_PRICE` and `AGE`
- **What to note**: Does older property age increase or decrease purchase price? By how much? This is a headline finding — it's counterintuitive in some markets.

### Offer per SQM ratio by sales type
- **What to note**: Which sales type commands the highest offer per SQM? This tells you where market demand is concentrated.

---

## Page 3 — 📌 Property type findings

### Offer vs. purchase price by house type
- **What to note**: Which house type has the largest gap between offer and final price? This signals negotiation dynamics per type.

### Interest rate & inflation by house type
- **What to note**: Which house types were most purchased during high-rate periods? Does type correlate with buyer sensitivity to macro conditions?

### SQM vs. SQM price combo chart
- **What to note**: Is there a house type that is large in SQM but cheap per SQM, or small but expensive? This is the value-density insight.
---

s what's actually driving value."
