# Streaming Platform Content Performance & Audience Retention Analytics

**Data Analyst:** Symone Thompson  
**Client/Sponsor:** Global Streaming Entertainment Operations & Programming Logistics  

---

## 🎯 Purpose
The purpose of this project is to address high-stakes production budget allocation and content viability challenges across a global streaming platform catalog. While superficial tracking models rely entirely on short-term trending metrics (such as a title briefly peaking on a Top 10 chart), true platform stability requires a deep evaluation of initial marketplace returns weighed against multi-week audience engagement decay. By evaluating raw production investments and historical catalog trends, this project isolates the explicit content profiles, genre bottlenecks, and high-cost retention thresholds that trigger abrupt, real-world content cancellations.

---

## 🚫 Out of Scope (Project Exclusions)
* **Real-Time Ad-Revenue Monetization:** Live streaming API data capture and individual subscriber ad-impression micro-transactions are entirely outside the scope of this analytics sprint.
* **Social Media Sentiment Extraction:** External platform scraping (e.g., parsing unstructured user text data or review threads from Reddit or X) is excluded from this structured relational data model.
* **Live User Demographics Mapping:** Tracking real-time subscriber account profiles or geolocation streaming metrics is not included in this catalog evaluation.

---

## 📦 Deliverables
* **SQL Optimization Engine Scripts:** Clean, production-ready, and well-commented `.sql` files executing baseline ROI calculations, multi-week retention coefficients, and high-risk budget risk modeling using Google BigQuery standard SQL syntax.
* **Cleaned Operational Datasets:** A curated data inventory containing baseline catalog configurations, processed retention coefficients, and high-budget risk assessments stored within the `Data_Cleaned/` directory.
* **Executive Summary SOW Documentation:** Formally structured Scope of Work documents mapping out project boundaries, schemas, milestones, and data validation logs for strategic platform programming leadership.
> 📊 **Analytical Scale Note:** All financial investment metrics (`Budget_usd`, `Box_Office_Revenue_usd`, and `baseline_profit`) are recorded in **USD ($)**. For high-level executive reporting, these baseline figures scale into the **millions of dollars** (e.g., a record displaying `101800000` represents **$101.8M USD**). The `baseline_roi` column represents a pure percentage ratio format.
---

## 🗓️ Schedule Overview & Project Milestones
Project execution is structured across highly focused technical milestones:
* **Phase 1: Ingestion & Baseline Auditing |** Access the Google BigQuery console sandbox environment, connect to the catalog table schemas, and isolate initial variables to validate core ROI investment benchmarks.
* **Phase 2: Retention Coefficient Analytics |** Draft, test, and execute advanced multi-week viewership decay query logic utilizing `ORDER BY ASC` sorting rules to identify hidden platform drops.
* **Phase 3: High-Budget Risk Modeling & Closure |** Synthesize financial investment weights against active retention floors to isolate top-tier cost bottlenecks and deploy finalized portfolio code assets directly to GitHub.

---

## 📊 Scenario 1: Baseline Structural Audit (Unsorted Exploration)
* **Objective:** Ingest the raw entertainment catalog data within the GCP sandbox to map out the distribution of production costs relative to genre categories, verifying baseline schema structures without sorting overrides or secondary active filters.
* **The SQL Logic:**
```sql
SELECT
`Movie Title`,
`Genre_1`,
`Budget_usd`,
`Box Office Revenue_usd`,
-- Calculate raw baseline profit margins
(`Box Office Revenue_usd` - `Budget_usd`) AS `baseline_profit`,
-- Calculate percentage ROI to establish a performance benchmark
ROUND((`Box Office Revenue_usd` - `Budget_usd`) / `Budget_usd`, 2) AS `baseline_roi`
FROM
 `healthy-bonsai-231119.Movie_Data.Movie_Data_Scenario_1`
ORDER BY
 `baseline_roi` DESC;
```

