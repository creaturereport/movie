# Phase 2: Audience Retention Decay Tracking & Platform Viability

### The Portfolio Scenario
**Project Track:** Viewership Decay & Retention Coefficient Tracking  
**Data Analyst:** Symone Thompson  
**Client/Sponsor:** Global Streaming Entertainment Operations & Programming Logistics  
**Target Asset:** `02_processed_retention_coefficients.csv`

---

## Executive Summary & Objective
The objective of Phase 2 is to isolate media properties experiencing catastrophic viewership decay immediately following their initial premiere frames. While superficial industry trackers focus heavily on short-term trending metrics, this analysis develops a custom **Retention Coefficient** to measure sustained user engagement. By sorting performance data in ascending order, this script uncovers the explicit programming profiles that fail to maintain audience loyalty.

---

## Deliverables & Schema Mapping

*A specific list of fields that this project phase delivers to the analytics inventory.*

| Column Name | Data Type | Analytical Purpose |
| :--- | :--- | :--- |
| `Movie_Title` | STRING | Serves as the unique property identifier across the global streaming catalog. |
| `Genre_1` | STRING | Macro-level content categorization used to isolate decay trends by vertical. |
| `baseline_profit` | FLOAT | Calculated margin baseline used to weigh financial loss against viewer decay. |
| `retention_coefficient` | FLOAT | Primary algorithmic ratio tracking sustained multi-week audience engagement floors. |

---

## Schedule & Milestones
* **Milestone 4 (June 22nd, 2026):** Development and execution of ascending retention sorting arrays in Google BigQuery.
* **Milestone 5 (June 22nd, 2026):** Exporting clean audience decay tabular models into the repository runtime directory.

---

## The Analytical Imperative
In streaming metrics, a severe multi-week decay coefficient is the leading indicator of sudden series cancellations. High box office numbers or massive initial premiere spikes mean nothing if the retention ratio drops below sustainable operational thresholds. This analysis provides data architecture visibility to help leadership proactively drop low-retention programming assets before downstream server costs outweigh long-term subscriber engagement.
