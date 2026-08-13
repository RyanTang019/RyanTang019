

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
<h1 align="center">Ryan Tang Shi Jie</h1>

<p align="center">
  <b>Economics & Data Science @ NTU · Class of 2027 · Singapore</b><br>
  I build data platforms that run in production — self-hosted orchestration, infrastructure as code, and tests that gate every deploy.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/ryan-tang-89975128a/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <img src="https://img.shields.io/badge/Singapore-EF3340?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Singapore">
  <img src="https://img.shields.io/badge/Open%20to-Data%20Engineering%20Internships-2ea44f?style=for-the-badge" alt="Open to internships">
</p>

---

## Projects

### [Singapore EV Infrastructure Data Platform](https://github.com/RyanTang019/Singapore-EV-Pipeline)

<a href="https://github.com/RyanTang019/Singapore-EV-Pipeline">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=RyanTang019&repo=Singapore-EV-Pipeline&bg_color=00000000&text_color=7d8590&title_color=58a6ff&icon_color=58a6ff&border_color=30363d" alt="Singapore EV Pipeline">
</a>

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Dagster](https://img.shields.io/badge/Dagster-4F43DD?style=flat-square&logo=dagster&logoColor=white)
![dbt](https://img.shields.io/badge/dbt%20Core-FF694B?style=flat-square&logo=dbt&logoColor=white)
![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?style=flat-square&logo=googlebigquery&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white)

A production ELT platform on a 2 vCPU / 4 GB Hetzner VM — self-hosted Dockerized Dagster and PostgreSQL orchestrating **three LTA feeds every 30 minutes** into BigQuery.

- **20 dbt models** across staging, intermediate, fact, dimension and reporting layers, with geospatial SQL and data-quality gates covering **all 55 Singapore planning areas**
- Configuration-driven ingestion framework with reusable OData and presigned-S3 extractors, dynamic pagination, exponential retries and append-only JSON landing
- **Terraform** provisions everything — VM, static IP, firewall, cloud-init, isolated dev/prod BigQuery datasets, IAM, Secret Manager, keyless CI identity, GCS-backed remote state
- **GitHub Actions** runs **80+ Python/dbt validation tests** before building SHA-versioned Docker images; nothing deploys until every check passes

### [Air Canada Reddit Customer Support Pipeline](https://github.com/RyanTang019/AirCanada-CustomerSupport)

<a href="https://github.com/RyanTang019/AirCanada-CustomerSupport">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=RyanTang019&repo=AirCanada-CustomerSupport&bg_color=00000000&text_color=7d8590&title_color=58a6ff&icon_color=58a6ff&border_color=30363d" alt="Air Canada Customer Support Pipeline">
</a>

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Airflow](https://img.shields.io/badge/Apache%20Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat-square&logo=snowflake&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white)

End-to-end ETL turning unstructured airline complaints into a triageable dataset.

- Ingests Reddit API data, normalizes **13 fields**, and loads Snowflake through **idempotent SQL MERGE** — re-runs never double-count
- Conditional branching and dynamic task mapping classify posts across **9 issue categories and 3 priority tiers**, with Pydantic schema validation at the boundary
- Airflow CeleryExecutor containerized with Docker Compose, Redis and PostgreSQL; automated priority-ranked email digests; RSA key-pair auth with environment-managed secrets

### [Fraud Detection System](https://github.com/RyanTang019/Fraud-Detection-Project)

<a href="https://github.com/RyanTang019/Fraud-Detection-Project">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=RyanTang019&repo=Fraud-Detection-Project&bg_color=00000000&text_color=7d8590&title_color=58a6ff&icon_color=58a6ff&border_color=30363d" alt="Fraud Detection Project">
</a>

![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat-square&logo=apachespark&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Parquet](https://img.shields.io/badge/Parquet-50ABF1?style=flat-square&logo=apacheparquet&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)

Fraud classification over **590,000+ credit card transactions**, built for the class-imbalance problem rather than around it.

- **92.87% AUC-ROC**, with **87% recall at 84% precision** on a 3.5% positive class — tuned with weighted loss functions, because a missed fraud costs more than a false alarm
- **58 engineered features** from velocity checks, temporal patterns and behavioral aggregations — a 15% lift over baseline
- Benchmarked Logistic Regression, Random Forest and Gradient Boosted Trees
- CSV → Parquet cut storage **88% (651 MB → 78 MB)** and loading **11x faster**

---

## Toolbox

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![R](https://img.shields.io/badge/R-276DC3?style=flat-square&logo=r&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)

**Orchestration & Transform**

![Dagster](https://img.shields.io/badge/Dagster-4F43DD?style=flat-square&logo=dagster&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white)
![Spark](https://img.shields.io/badge/PySpark-E25A1C?style=flat-square&logo=apachespark&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)

**Warehouses & Storage**

![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?style=flat-square&logo=googlebigquery&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat-square&logo=snowflake&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

**Infrastructure**

![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

**Analytics & BI**

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=flat-square&logo=tableau&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

**Learning next** — Kafka, Flink, ClickHouse. Moving from batch into streaming.

---

## Notes

I write up what I learn as I go — [Obsidian-Brain](https://github.com/RyanTang019/Obsidian-Brain) and [llm_wiki](https://github.com/RyanTang019/llm_wiki) are my working notes on data infrastructure and LLM systems.
