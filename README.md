Project Overview:

  An end-to-end healthcare analytics platform built on CMS Synthetic Public Use Files (SynPUF). This project transforms raw, fragmented Medicare enrollment and claims data into a dimensional Star Schema, powering a suite of   Power BI dashboards designed for actuarial analysis, financial tracking, and compliance.

Business Value & Dashboards:

  This repository contains the data models, DAX measures, and dashboard specifications that solve four primary healthcare analytics challenges:
 
  Member Demographics & Financial Risk (Population Health): 
    Transitions raw eligibility data into actionable risk profiles. By bridging demographic volume with financial cost (Spend PMPY), this module allows population health managers to forecast financial reserves and                allocate resources to high-risk cohorts (e.g., ESRD patients).

   Macro Claims & Financials (Single Source of Truth): 
    Solves the fragmented billing problem by unifying Inpatient, Outpatient, and Carrier claims via a conformed Star Schema. This provides finance teams with a unified ledger to instantly track total cost of care and            attribute disease burden spend.

  Provider Utilization & FWA Detection (Cost Containment):
    An automated scorecard and anomaly detection engine for network managers. By tracking efficiency metrics like Average Length of Stay (LOS) against a statistical baseline, it visually isolates inefficient                     facilities and flags potential Fraud, Waste, and Abuse (FWA) for compliance teams.

  Pharmacy Analytics (Part D Integration): 
    Breaks down data silos by creating a dimensional crosswalk between FDA National Drug Codes (NDCs) and Part D claims. Enables clinical pharmacists to track medication adherence, patient out-of-pocket burden, and              top-spend therapeutic classes alongside medical history.

Technical Architecture:

  Data Ingestion: Databricks Auto Loader (Streaming to Batch)

  Data Processing: PySpark & Delta Lake (Medallion Architecture: Bronze ➔ Silver ➔ Gold)

  Data Modeling: Dimensional Star Schema optimized for BI

