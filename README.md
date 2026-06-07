# Operational Asset & Work Order Analytics

## Project Overview
End-to-end MRO operations analytics solution simulating 
a maintenance tracking system for an aviation/industrial 
organisation. Built to demonstrate SQL, Python, and 
Power BI capabilities in an operational context.

## Tech Stack
- Python 3 + Faker — synthetic data generation
- SQLite — relational database
- SQL — 12 queries across 3 complexity levels
- Power BI Desktop — 4-page interactive dashboard
- DAX — 13 custom measures

## Dataset
- 500 work orders across 30 assets and 20 technicians
- 5 normalized tables: assets, technicians, work_orders,
  work_order_costs, sla_definitions
- Full year 2023 with realistic distributions

## Dashboard Pages
1. Work Order Overview — operational status and trends
2. SLA Compliance — breach analysis by priority and technician
3. Cost Analysis — spend tracking vs $1.53M annual target
4. Asset Downtime — reliability analysis by asset and type

## Key Findings
- Critical priority SLA compliance: 0% 
  (4hr target consistently missed)
- Annual budget exceeded by 11.1% in November 2023
- Preventive maintenance has highest SLA breach count (50)
  despite being fully scheduled in advance
- Airbus E175 #026 — highest annual downtime at 664 hours
- Dylan Miller (Lead technician) — 57.14% breach rate,
  worst performer at the most senior level

## SQL Concepts Demonstrated
- Aggregations and GROUP BY
- Multi-table JOINs
- Subqueries and conditional aggregation
- Window functions: RANK(), LAG(), SUM() OVER
- CTEs for staged computation

## How to Run
1. Clone the repository
2. Run `pip install faker` 
3. Run `python data/generate_data.py`
4. Open `dashboard/MRO_Analytics.pbix` in Power BI Desktop
5. Update CSV file paths in Power Query if needed
