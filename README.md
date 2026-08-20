# TRA Watch

## Problem Statement
TRA's trade remedies data — investigation cases, commodity flows, 
tariff decisions, and country patterns — is publicly available but 
scattered, unstructured, and disconnected from HMRC trade data. 

There is no unified platform that engineers this data end to end, 
surfaces patterns across anti-dumping, anti-subsidy, and safeguard 
investigations, measures tariff effectiveness, and makes it all 
queryable through AI.

TRA Watch builds that platform.

## What TRA Watch Does
- Ingests TRA public investigation data and HMRC trade flow data
- Engineers it through a medallion architecture (bronze/silver/gold)
- Detects patterns across dumping, subsidy and safeguard cases
- Measures whether tariff decisions actually worked
- Makes all of it queryable through an AI layer in plain English

## Stack
- **Infrastructure:** Terraform, GitHub Actions
- **Ingestion:** Azure Data Factory
- **Storage:** Azure Data Lake Gen2, Delta Lake, Microsoft Dataverse
- **Processing:** Databricks
- **Governance:** Unity Catalog, Azure Key Vault
- **Data Quality:** Great Expectations, Power BI
- **Reporting:** Power BI
- **Monitoring:** Azure Monitor, Azure Log Analytics
- **AI Layer:** LangChain, Azure OpenAI, Azure AI Search, MLflow

## Architecture
Medallion architecture — bronze, silver, gold layers

- **Bronze** — raw data, untouched
- **Silver** — cleaned, validated, SCD Type 2, Data Vault
- **Gold** — aggregated, reporting ready

## Branching Strategy
- `main` — production
- `testing` — integration tests
- `dev` — development
- `feature/*` — individual features

## Data Sources
- TRA Public Investigations Repository
- HMRC UK Trade Info Bulk Datasets

## Author
Kingsley Okonkwo — Grade 7 Data Engineer