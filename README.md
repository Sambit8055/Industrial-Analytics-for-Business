# Production Planning, Plan-vs-Actual & Capacity Optimization

## Project Overview
An end-to-end manufacturing analytics project designed around production planning, MIS reporting, capacity utilization, machine availability, downtime and Plan-vs-Actual analysis.

The project simulates a high-volume manufacturing environment and converts operational data into management-ready KPIs and decision support.

## Business Problem
Production leadership needs visibility into:
- Planned vs actual output
- Production variance and loss
- Machine utilization and capacity utilization
- Downtime impact
- Material and manpower constraints
- Machine/shift bottlenecks
- Monthly production trends

## Objectives
1. Measure Plan Achievement.
2. Identify major production gaps.
3. Analyze machine and shift utilization.
4. Quantify production loss caused by downtime and constraints.
5. Identify bottleneck machines.
6. Create an executive-ready reporting structure.

## Tools
- Microsoft Excel
- Power Query concepts
- Power BI
- SQL-ready data model
- Python/Pandas for data preparation

## Dataset
`data/production_planning_dataset.csv`

Rows: 5,200

The dataset contains production records with planning, output, downtime, material, manpower and utilization fields.

## Key KPIs
- Plan Achievement %
- Production Variance
- Production Loss
- Machine Utilization %
- Capacity Utilization %
- Downtime Hours
- Below Target %
- Actual vs Planned Production

## Analytical Approach
1. Data collection / simulation
2. Data validation
3. Cleaning and transformation
4. KPI calculation
5. Plan-vs-Actual analysis
6. Machine-level analysis
7. Monthly trend analysis
8. Constraint and loss analysis
9. Management recommendations

## Example DAX Measures

```DAX
Total Planned = SUM(Production[Planned_Production])

Total Actual = SUM(Production[Actual_Production])

Production Loss =
[Total Planned] - [Total Actual]

Plan Achievement % =
DIVIDE([Total Actual], [Total Planned], 0)

Average Machine Utilization % =
AVERAGE(Production[Machine_Utilization_%])

Total Downtime Hours =
SUM(Production[Downtime_Hours])
```

## Recommended Power BI Pages
1. Executive Overview
2. Plan vs Actual
3. Machine & Capacity Analysis
4. Downtime & Production Loss
5. Shift/Trend Analysis

## Business Insights
The analysis should focus on machines and periods with persistent plan achievement below target, high downtime and low utilization. These areas can then be prioritized for capacity balancing, preventive maintenance, material planning and manpower alignment.

## Resume Project
**Production Planning & Capacity Optimization Analytics | Excel, Power BI, Power Query**

Developed an end-to-end manufacturing analytics solution to monitor Plan-vs-Actual production, machine utilization, capacity utilization, downtime and production losses. Built KPI dashboards and machine-level analysis to identify bottlenecks, quantify production gaps and support data-driven production planning decisions.

## Portfolio
Use the report in `docs/Production_Planning_Project_Report.pdf` as the detailed case study.

## Repository Structure
```text
Production_Planning_Capacity_Optimization/
├── data/
│   └── production_planning_dataset.csv
├── docs/
│   └── Production_Planning_Project_Report.pdf
├── excel/
│   └── Production_Planning_Capacity_Optimization.xlsx
├── powerbi/
│   └── PowerBI_Dashboard_Specification.md
├── python/
│   └── analysis_template.py
├── README.md
└── requirements.txt
```

## Disclaimer
This is a portfolio project using a simulated industrial dataset. It is designed to demonstrate analytical methodology and dashboard development; it does not represent confidential employer data.
