

<!--
**RyanTang019/RyanTang019** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

# Ryan Tang Shi Jie

**Economics & Data Science @ NTU (Class of 2027) · Singapore**

I build data platforms that run in production — self-hosted orchestration, infrastructure as code, and tests that gate every deploy.

**Currently looking for:** Data Engineering / Data Analytics internships in Singapore.

---

## [Singapore EV Infrastructure Data Platform](https://github.com/RyanTang019/Singapore-EV-Pipeline)
`Python` · `SQL` · `Dagster` · `dbt Core` · `BigQuery` · `Terraform` · `Docker` · `GitHub Actions` · `GCP` · `Hetzner`

A production ELT platform running on a 2 vCPU / 4 GB Hetzner VM — self-hosted Dockerized Dagster and PostgreSQL orchestrating **three LTA feeds every 30 minutes** into BigQuery.

- **20 dbt models** across staging, intermediate, fact, dimension and reporting layers, with geospatial SQL and data-quality gates covering **all 55 Singapore planning areas**
- Configuration-driven ingestion framework with reusable OData and presigned-S3 extractors, dynamic pagination, exponential retries and append-only JSON landing
- **Terraform** provisions everything — VM, static IP, firewall, cloud-init, isolated dev/prod BigQuery datasets, IAM, Secret Manager, keyless CI identity, GCS-backed remote state
- **GitHub Actions** runs **80+ Python/dbt validation tests** before building SHA-versioned Docker images; nothing deploys until every check passes

## [Air Canada Reddit Customer Support Pipeline](https://github.com/RyanTang019/AirCanada-CustomerSupport)
`Python` · `Apache Airflow` · `Snowflake` · `Docker` · `Pydantic`

End-to-end ETL turning unstructured airline complaints into a triageable dataset.

- Ingests Reddit API data, normalizes **13 fields**, and loads Snowflake through **idempotent SQL MERGE** — re-runs never double-count
- Conditional branching and dynamic task mapping classify posts across **9 issue categories and 3 priority tiers**, with Pydantic schema validation at the boundary
- Airflow CeleryExecutor containerized with Docker Compose, Redis and PostgreSQL; automated priority-ranked email digests; RSA key-pair auth for Snowflake with environment-managed secrets

## [Fraud Detection System](https://github.com/RyanTang019/Fraud-Detection-Project)
`PySpark` · `MLlib` · `Python` · `Parquet`

Fraud classification over **590,000+ credit card transactions**, built for the class-imbalance problem rather than around it.

- **92.87% AUC-ROC**, with **87% recall at 84% precision** on a 3.5% positive class — tuned with weighted loss functions, because a missed fraud costs more than a false alarm
- **58 engineered features** from velocity checks, temporal patterns and behavioral aggregations — a 15% lift over baseline
- Benchmarked Logistic Regression, Random Forest and Gradient Boosted Trees
- CSV → Parquet cut storage **88% (651 MB → 78 MB)** and loading **11x faster**

---

## Toolbox

| | |
|---|---|
| **Languages** | Python (Pandas, NumPy, PySpark, PyTorch), SQL, R, C |
| **Orchestration & Transform** | Dagster, Airflow, dbt Core |
| **Warehouses & Storage** | BigQuery, Snowflake, PostgreSQL, DuckDB, Parquet |
| **Infrastructure** | Terraform, Docker, GitHub Actions, GCP, Hetzner Cloud |
| **Analytics & BI** | Power BI, Tableau, Streamlit |
| **Learning next** | Kafka, Flink, ClickHouse — moving from batch into streaming |

## Notes

I write up what I learn as I go — [Obsidian-Brain](https://github.com/RyanTang019/Obsidian-Brain) and [llm_wiki](https://github.com/RyanTang019/llm_wiki) are my working notes on data infrastructure and LLM systems.

## Reach me

[LinkedIn](https://www.linkedin.com/in/ryan-tang-89975128a/) · Singapore
