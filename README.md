# movie 

**I ran into a need to do some data cleaning to transpose the data from Google Sheets > Google BigQuery that I thought were important to document (from a learners standpoint).Here are troublehooting notes taken to troubleshoot :

+ Source Data Sovereignty: Resolving complex characters like () with standard snake_case _ at the source spreadsheet saves hours of syntax debugging later.

+ Exact Relational Mapping: Ensuring naming conventions match your physical schemas exactly eliminates false errors like that location glitch.

+ Schema Ingestion Awareness: Trusting Auto detect but actively auditing the result keeps your data clean.
