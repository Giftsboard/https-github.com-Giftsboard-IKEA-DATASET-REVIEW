# 📊 Sales Performance Dashboard | Power BI

> My very first Power BI project (2023): an exploration of where a retail business makes money, and where it quietly loses it.

![Dashboard Preview](images/dashboard.png)
<!-- Export your dashboard as a PNG and save it at images/dashboard.png -->

---

## 📌 Table of Contents

1. [Project Overview](#-project-overview)
2. [Business Problem](#-business-problem)
3. [Objectives](#-objectives)
4. [Dataset](#-dataset)
5. [Tools & Skills Used](#-tools--skills-used)
6. [Dashboard Walkthrough](#-dashboard-walkthrough)
7. [Key Insights](#-key-insights)
8. [Recommendations](#-recommendations)
9. [Limitations & Lessons Learned](#-limitations--lessons-learned)
10. [Repository Structure](#-repository-structure)
11. [How to Use This Project](#-how-to-use-this-project)
12. [About Me](#-about-me)

---

## 🧭 Project Overview

This project is an interactive Power BI dashboard that analyses sales performance across **states, years, quarters and product categories** (Furniture, Office Supplies and Technology) for the period **2014 to 2017**.

It was built in 2023 as my first end-to-end Power BI project. The goal was simple: take raw sales data and turn it into visuals that help a decision-maker see what is driving profit and what is draining it.

---

## 💡 Business Problem

Sales volume can look healthy while profit quietly leaks away. In this dataset, a small number of states and one product category wiped out the gains made elsewhere, leaving the business with a **small net loss of about $124.51** over the four years.

Leadership needed answers to questions like:

- Which product categories actually make money?
- Which states are profitable, and which are losing money?
- How did profit change from year to year?
- Is there a seasonal pattern in profitability?
- Where is volume being sold at the expense of profit?

---

## 🎯 Objectives

- Analyse profit and quantity sold by **state, year, quarter and category**
- Identify the **top and bottom performing** categories and regions
- Spot **trends and anomalies** over time
- Present findings in a single, easy-to-read dashboard
- Provide **actionable recommendations** to improve profitability

---

## 🗂 Dataset

| Detail | Description |
|---|---|
| **Source** | `[Add dataset source / link here]` |
| **Time period** | 2014 to 2017 |
| **Granularity** | Order-level sales records |
| **Key fields used** | State, Category, Ship Date (Year / Quarter), Profit, Quantity |

> **Note:** Add a short description of how the data was obtained and any cleaning or transformation you did in Power Query (for example: removed duplicates, fixed data types, created date hierarchies).

---

## 🛠 Tools & Skills Used

- **Power BI Desktop** for data modelling and dashboard design
- **Power Query** for data cleaning and transformation
- **Date hierarchy** (Year and Quarter) built from Ship Date
- **Visualisation techniques:** matrix, donut chart, 100% stacked bar, stacked bar, filled map and Smart Narrative (AI-generated insights)

---

## 🖥 Dashboard Walkthrough

| Visual | What it shows |
|---|---|
| **Matrix: Profit by State and Year** | Profit for each state across 2014 to 2017, with row and column totals |
| **Donut chart: Profit by Quarter and Category** | How profit is distributed across ship-date quarters and categories |
| **Filled map: Profit by State and Category** | Geographic view of profit by state, coloured by category |
| **100% stacked bar: Profit by Year and Category** | How each category contributed to profit (or loss) every year |
| **Stacked bar: Quantity by State and Category** | Which states sell the most volume, and in which categories |
| **Smart Narrative** | Auto-generated text summarising top categories, averages and anomalies |

---

## 🔍 Key Insights

### Overall performance
- Total profit across 2014 to 2017 was **-$124.51**, a small net loss.
- **2014** (+$528.62) and **2016** (+$1,019.45) were profitable years, **2017** was marginal (+$92.96), and **2015** was a heavy loss year (**-$1,765.54**).

### Category performance
| Category | Total Profit | Average Profit |
|---|---|---|
| Technology | **$785.68** | $196.42 |
| Office Supplies | **$741.15** | $185.29 |
| Furniture | **-$1,651.34** | -$412.84 |

- **Technology** and **Office Supplies** are the profit engines.
- **Furniture** is the biggest drag and accounts for more than the entire net loss.
- The most recent profit anomaly was in **2016**, when Technology reached a high of **$476.33**.

### State performance
- 🌟 **Top profit contributors:** California ($506.55), New York ($449.50) and Kentucky ($261.49).
- 📉 **Biggest losses:** **Pennsylvania (-$1,648.95)**, mostly in 2015, and **Florida (-$370.95)**.
- Pennsylvania also ranks among the top states by quantity sold, which suggests volume is being sold at a loss.
- Illinois (-$47.61) and Oregon (-$3.79) also finished in the red.

### Volume
- **California** leads in quantity sold, making up about **12.53%** of total quantity.
- Other high-volume states include Texas, New York, Pennsylvania and Minnesota.

### Seasonality
- The largest single slice of the quarterly profit donut (**about 31.6%**) falls in **Q4**, hinting at a seasonal peak.

---

## ✅ Recommendations

1. **Review Furniture pricing and discounting.** It is the single biggest source of loss and should be the first priority.
2. **Investigate Pennsylvania and Florida.** Look at discount levels, shipping and logistics costs, and product mix to understand why high volume is not producing profit.
3. **Prioritise Technology and Office Supplies** in marketing spend and inventory planning, since they deliver consistent profit.
4. **Replicate what works** in California, New York and Kentucky (pricing, product mix, fulfilment) in weaker regions.
5. **Plan for Q4.** Secure stock levels and campaigns ahead of the seasonal peak.
6. **Dig into 2015.** Identify what caused the sharp drop that year (for example one-off discounts, a bad product line or large unprofitable orders) so it is not repeated.

---

## 🌱 Limitations & Lessons Learned

This was my first Power BI project, and I am keeping it as it was to show my starting point. Looking back, here is what I would do differently today:

- **Add KPI cards** (Total Sales, Total Profit, Profit Margin, Quantity) so the headline numbers are visible immediately.
- **Add slicers** for year, category and region to make the report more interactive.
- **Use drill-through pages** to explore problem states such as Pennsylvania in detail.
- **Include discount and shipping cost analysis** to explain *why* losses occur, not just where.
- **Write DAX measures** (such as profit margin and year-over-year growth) instead of relying only on raw sums.
- **Replace the legacy map visual** with the newer Azure Maps visual, since Power BI is retiring the old one.
- **Verify the Q4 finding** with a dedicated quarter-only visual, since the donut mixes quarter and category slices.

**Biggest lesson:** a good dashboard is not about pretty charts. It is about asking the right questions and turning data into decisions.

---

## 📁 Repository Structure

```
├── README.md
├── data/
│   └── sales_data.csv            # Dataset used (or link to source)
├── dashboard/
│   └── Sales_Dashboard.pbix      # Power BI file
├── images/
│   └── dashboard.png             # Dashboard screenshot
└── Sales_Dashboard.pdf           # PDF export of the dashboard
```

> Update this structure to match your actual repository.

---

## ▶️ How to Use This Project

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   ```
2. **Install Power BI Desktop** (free) from the [Microsoft website](https://powerbi.microsoft.com/desktop/).
3. **Open** `dashboard/Sales_Dashboard.pbix` in Power BI Desktop.
4. If prompted, **update the data source path** under *Transform data → Data source settings* to point to the `data` folder on your machine.
5. Explore the visuals and click on elements to cross-filter the report.

---

## 👤 About Me

**[Your Name]**
Data Analyst | Power BI | [Add other skills, e.g. SQL, Excel, Python]

- 💼 LinkedIn: [your-linkedin-url]
- 📧 Email: [your-email]
- 🌐 Portfolio: [your-portfolio-url]

---

⭐ If you found this project useful or inspiring, consider giving the repo a star![IKEA Reatil Dashboard.pdf](https://github.com/user-attachments/files/33227081/IKEA.Reatil.Dashboard.pdf)
