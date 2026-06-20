# Sales & Financial Performance Dashboard

An interactive, browser-based dashboard built for the **Data Analyst Internship – Task 3: Dashboard Design**.

Built with **HTML, CSS, and JavaScript (Chart.js)** instead of Power BI / Tableau, since those tools require desktop installation. This approach delivers the same outcome — an interactive dashboard that informs business decisions — as a single file that runs in any browser, no installation required.

## How to view it

1. Download `index.html` and `bundle.js` (keep them in the same folder).
2. Double-click `index.html` — it opens directly in your browser. No server, no installation.

## Dataset

`Financials.csv` — the "Financial Sample" dataset (700 transactions, FY2013–2014), covering:
- **Segment**: Government, Small Business, Enterprise, Midmarket, Channel Partners
- **Country**: USA, Canada, France, Germany, Mexico
- **Product**: Paseo, VTT, Velo, Amarilla, Montana, Carretera
- **Metrics**: Units Sold, Gross Sales, Discounts, Sales, COGS, Profit

## Dashboard features (mapped to task requirements)

| Requirement | Implementation |
|---|---|
| a. Right KPIs | Total Sales, Total Profit, Profit Margin %, Units Sold — with YoY growth indicators |
| b. Slicers/filters | Year, Segment, Country, Product dropdowns — all charts and KPIs update live |
| c. Time-series analysis | Monthly Sales & Profit trend line chart |
| d. Cards for totals/summary | Four KPI cards at the top of the Overview page |
| e. Consistent color theme | Navy / ice-blue corporate palette used throughout |
| f. Navigation menu | Two-page nav: **Overview** (KPIs + trends) and **Product & Market Detail** (breakdowns + sortable transaction table) |

## Key insights from the data

- Total Sales: **$118.7M** | Total Profit: **$16.9M** | Overall Profit Margin: **14.2%**
- Sales grew **~250% year-over-year** from 2013 to 2014.
- **Government** is the largest segment by sales, followed by Small Business.
- **Paseo** is the best-selling product line.
- Profit margin **drops sharply as discount band increases** — "High" discount transactions have roughly a third of the margin of "None" discount transactions, suggesting discounting is eroding profitability faster than it's driving volume.

## Tools used

- HTML/CSS/JavaScript
- [Chart.js](https://www.chartjs.org/) (bundled locally, no internet required to run)
- Python/pandas (for initial data cleaning — see note below)

## Notes on data cleaning

The raw CSV stores currency columns (including, unusually, "Units Sold") as text with `$` signs and comma thousands-separators, and negative numbers in accounting format e.g. `$(35,550.00)`. These were cleaned and converted to numeric types before building the dashboard. A handful of rows had a blank `Profit` value; these were recalculated as `Sales − COGS`.
