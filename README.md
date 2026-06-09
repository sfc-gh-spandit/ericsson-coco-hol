# Ericsson x Snowflake — Cortex Code Hands-on Lab

Build a complete data pipeline and conversational AI agent from raw SEC insider trading data using Snowflake Cortex Code.

## What You'll Build

```
Marketplace Data → Bronze (CTAS) → Silver (Dynamic Tables) → Gold (Denormalized) → Cortex Agent
```

In ~90 minutes you'll go from raw public SEC filings to a natural language analytics interface — entirely through AI-assisted prompts in Cortex Code.

## Prerequisites

- A Snowflake trial account (or any account with SYSADMIN + ACCOUNTADMIN access)
- Cortex Code installed ([download here](https://docs.snowflake.com/en/user-guide/ui-snowsight/cortex-code))
- A working internet connection

## Getting Started

1. Download **`Ericsson_CoCo_HOL.html`** from this repo
2. Open it in your browser (Chrome, Edge, Safari, or Firefox)
3. Follow the step-by-step guide — each phase has copy-paste prompts

## Lab Structure

| Phase | Topic | Duration | Snowflake Features |
|-------|-------|----------|-------------------|
| 0 | Setup | ~15 min | Connection, Marketplace, AGENTS.md |
| 1 | Bronze Layer | ~15 min | CTAS, Medallion Architecture |
| 2 | Data Quality & Streams | ~18 min | DMFs, Streams, Stored Procedures |
| 3 | Silver Layer | ~25 min | Dynamic Tables, 3NF Normalization |
| 4 | Gold Layer | ~10 min | Denormalized Wide Tables, DT DAG |
| 5 | AI Layer | ~15 min | Semantic Views, Cortex Agents |

## Data Source

Free public SEC insider trading data from the [Snowflake Marketplace](https://app.snowflake.com/marketplace/listing/GZTSZ290BV255) — 16.7M+ real insider trading filings. No cost, no signup required beyond your Snowflake account.

## Support

If you run into issues during the lab, check the troubleshooting notes in each phase of the guide. Common fixes:

- **"Database not found"** → Install the marketplace listing (link in Setup phase)
- **Permission errors** → Switch to ACCOUNTADMIN: `/sql USE ROLE ACCOUNTADMIN;`
- **Cortex Agent fails** → Ensure cross-region inference is enabled (Setup phase, step 3)
