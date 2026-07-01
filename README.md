# Restaurant Chain Pipeline

End-to-end Databricks data engineering project for restaurant analytics, combining synthetic data generation, streaming ingestion, medallion transformations, and dashboard-ready gold models.

<img width="1426" height="671" alt="Restaurant Chain Architecture" src="https://github.com/user-attachments/assets/167dec49-d789-4e6c-846d-fdc6fbf60a1c" />


## What This Repository Contains

- Synthetic data generators for restaurants, menu, customers, orders, and reviews.
- Event Hub order streaming simulator.
- Bronze, silver, and gold pipeline transformations.
- Gold models used for performance and review intelligence dashboards.

## Dashboard Demos

### Master Dashboard

Key features:

- Date-range filtering (`start_date`, `end_date`) for period-over-period analysis.
- KPI cards for Total Orders, Total Revenue, Active Customers, and AOV.
- Daily sales trend to monitor growth and seasonality.
- Best-selling items view for menu performance optimization.
- Order volume by day of week and peak-hour heatmap (day x hour) for staffing decisions.
- Revenue split by order type (`dine_in`, `takeaway`, `delivery`) and food category mix.


https://github.com/user-attachments/assets/a8cc4b14-2d53-4362-b2a6-5974a5eb3ca6


### Customer Insights

Key features:

- Restaurant-level filtering to compare customer sentiment by location.
- Review volume and sentiment trend over time (positive, neutral, negative).
- Average rating and rating distribution for quality benchmarking.
- Sentiment counts with quick split across positive/neutral/negative reviews.
- Issue categorization for operational root causes: delivery, food quality, pricing, portion size.
- Recent review feed for real-time voice-of-customer monitoring.

https://github.com/user-attachments/assets/1f3f57c5-e7f6-4c9b-b3fa-30fba6213beb


## Quick Start

1. Install Python dependencies:

```bash
pip install -r requirements.txt
pip install -r projects/databricks-e2e-project/00_synthetic_data/requirements.txt
```

2. Generate base synthetic datasets:

```bash
cd projects/databricks-e2e-project/00_synthetic_data
python 03_run.py
```

3. Stream live orders to Event Hub (optional for real-time ingestion tests):

```bash
python 04_eventhub_orders.py
```

4. Run Databricks ingestion and transformation pipelines from the project pipeline folder.

## Full Project Documentation

For architecture details, table-level design, setup order, dashboards, and troubleshooting, see:

- [Detailed README](projects/databricks-e2e-project/README.md)

## Useful Paths

- [Project folder](projects/databricks-e2e-project)
- [Synthetic data scripts](projects/databricks-e2e-project/00_synthetic_data)
- [Pipeline definitions](projects/databricks-e2e-project/01_pipelines)
- [Dashboard metrics](projects/databricks-e2e-project/dashboard_metrics.md)
