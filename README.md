# Restaurant Chain Pipeline

End-to-end Databricks data engineering project for restaurant analytics, combining synthetic data generation, streaming ingestion, medallion transformations, and dashboard-ready gold models.

# Dashboard

## Dashboard Demos

### Master Dashboard

<video src="dashboard/Master Dashboard.mp4" controls width="100%"></video>

[Open video directly](dashboard/Master%20Dashboard.mov)

### Customer Insights

<video src="dashboard/Customer Insights.mp4" controls width="100%"></video>

[Open video directly](dashboard/Customer%20Insights.mov)



![Project Architecture](projects/databricks-e2e-project/diagrams/project_architecture.png)

## What This Repository Contains

- Synthetic data generators for restaurants, menu, customers, orders, and reviews.
- Event Hub order streaming simulator.
- Bronze, silver, and gold pipeline transformations.
- Gold models used for performance and review intelligence dashboards.

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