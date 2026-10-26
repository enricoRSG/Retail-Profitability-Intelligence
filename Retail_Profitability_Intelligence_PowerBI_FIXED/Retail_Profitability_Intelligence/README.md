# Retail Profitability Intelligence | Power BI portfolio project

**Original end-to-end Power BI project (PBIP/PBIR), built with a self-contained synthetic retail dataset.**

## Quick start
1. Extract the entire ZIP to a normal local Windows folder (do not open inside ZIP).
2. Install the latest **Power BI Desktop** on Windows.
3. Double-click `Retail_Profitability_Intelligence.pbip`.
4. If prompted, select **Apply changes / Refresh** to generate the model with the included Power Query M scripts. No external datasource credentials or file paths are needed.
5. Save as `.pbix` in Power BI Desktop if you prefer a single-file deliverable. Verify the report visuals and model before publishing.

## Business problem
Executive reporting is often fragmented across spreadsheets. This dashboard unifies revenue, gross profit, discounts, returns and profitability by product, customer segment, channel and Italian sales region.

## Included reports
- 01 Executive overview — KPIs, monthly revenue, sales mix and filters.
- 02 Profitability drivers — profitability trend, discounts, COGS and return drivers.
- 03 Product performance — product-level profit, margin and units.
- 04 Channel & region — regional scorecard and channel profitability.

## Data architecture
Star schema: fact table **Sales** (4,800 simulated orders, 2024–2025) and dimensions **Dates, Products, Regions, Channels, Segments**. Single direction many-to-one relationships. Power Query M builds every table from deterministic inline data; refresh requires no cloud login and no absolute local paths.

## Metric glossary
Revenue = units × list price × (1 − discount) excluding full returns. COGS = units × unit cost excluding full returns. Gross profit = Revenue − COGS. Gross margin = Gross profit / Revenue. Return rate = returned orders / all orders. Year-over-year measures compare corresponding date-filter context using SAMEPERIODLASTYEAR.

## Data governance and limitations
All entities and transactions are **synthetic**, not from an actual employer/customer. The model assumes fully returned orders have zero recognized revenue and COGS, treats discounts as percentages of list price, and does not include shipping, overhead, taxes or inventory. It is a demonstration of reporting skill, not audited financial statements.

## Technology
Power BI Desktop, Power Query (M), DAX, Microsoft PBIP and PBIR open project formats, semantic data modeling.

## Verification status
All project JSON and model structure statically checked. This authoring environment cannot run Power BI Desktop, so **in-application refresh and rendering have not been verified**. Open the PBIP in Desktop and validate, then export to PBIX for client use.

## Portfolio CV snippet
Designed a multi-page Power BI retail profitability system featuring a relational star schema, 19 DAX measures and self-generated synthetic transactional data to analyze revenue, profit, margin, returns and regional/channel performance.
