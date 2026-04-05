# Post Project - Critical Analysis and Improvement Plan v0.1.0

## Objective
This project is a simple POC of data engineering pipeline using dbt. It follows the principle of Extract, Load and Transform

However, this project has its limitation.

## Limitations and Improvement Need in Pipeline Design
- We should not use `dbt seed` for data ingestion. `dbt seed` is used for uploading static tables.
- EDA is too basic, we need proper EDA even for data engineering purpose.
- Problem Statement is required to identify what problem this project tries to solved.
- Data acceptance criteria need to be set up.
- Data drift criteria need to be defined.
- EDA for data analysis should be performed
- dbt models need to be reviewed to satisfied business answer

## Improvement Plan

### Feature Improvement v0.2.0
- Remove `dbt seed` and implement `meltano`
- Instead of direct BigQuery loading from Python, we use Python to download data and perform data cleaning and save the data for ingestion.
- We use Meltano for ingestion using tap-csv

### Other Feature Improvement
- Complete full EDA for data engineering
- Identify answer to data engineering questions on schema, structure and latency
- Implement `dbt test` for data structure
- Identifying and define business analysis questions (based on minimum viable product)
- Review current staging tables and fact tables
- Setup simple dimension table or mart table according to the business question
- Improvement on testing and CI/CD setup
- Research on data ops
- Use Google Cloud Storage to keep a history of raw files
- Use DVC for data version control
- Implement measure to prevent downloading the same file using fingerprinting
- Replace full file update with incremental update
- Implement row based versioning
- Implement Evidently AI for data drift
- Explore other dbt products such as `Elementary`.
- Explore other data product such as Great Expectation, Soda and Monte Carlo.
