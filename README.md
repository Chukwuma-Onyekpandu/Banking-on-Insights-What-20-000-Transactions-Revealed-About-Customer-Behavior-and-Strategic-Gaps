# Banking-on-Insights-What-20-000-Transactions-Revealed-About-Customer-Behavior-and-Strategic-Gaps
# Banking Customer & Transaction Analysis

### Project by Onyekpandu Chukwuma
![Dashboard](https://github.com/Chukwuma-Onyekpandu/Banking-on-Insights-What-20-000-Transactions-Revealed-About-Customer-Behavior-and-Strategic-Gaps/blob/main/Screenshot%202025-06-25%20081721.png)
---

### Project Overview

This project presents a deep-dive analysis of a comprehensive banking dataset containing 20,000 transactions. The goal was to step into the role of a data analyst at a modern financial institution to understand customer behavior, optimize services, and inform strategic planning. Using Power BI, an interactive dashboard was developed to explore customer segmentation, transaction patterns, revenue streams, and trends over time.

### Problem Statement & Objectives

The analysis aimed to answer critical business questions to help the bank improve its performance and customer relationships:
- **Customer Segmentation:** Which customer segments are most active and profitable? What products do they prefer?
- **Transaction Behavior:** What are the dominant transaction types, channels, and branch hotspots?
- **Revenue Insights:** What are the primary drivers of fee-based revenue, and are certain customer groups incurring more costs?
- **Trend Analysis:** Are there seasonal peaks in activity, and are product recommendations aligned with customer behavior?

### Dataset

The analysis was performed on a synthesized dataset designed to mimic real-world banking transactions. It includes 20,000 enriched financial records across products like checking accounts, loans, mortgages, and card payments, with features covering customer demographics, transaction details, and financial metrics.

### Tools Used

- **Microsoft Power BI:** The primary tool for data modeling, creating DAX measures, and building the interactive dashboard.
- **Power Query:** Used for all data cleaning, transformation, and feature engineering.
- **DAX (Data Analysis Expressions):** Used to create a suite of KPIs and analytical measures.

---

### Data Preparation & Feature Engineering

To enable a robust analysis, several key data preparation and feature engineering steps were performed in Power Query:
- **Financial Flow Column:** An `ActualAmount` column was created using conditional logic (`if [TransactionType] = "Deposit" then [Amount] else -1 * [Amount]`) to accurately represent credits (positive) and debits (negative). This was critical for calculating net financial flow.
- **Date/Time Enhancement:** The `TransactionDate` column was used to generate several new columns for time-series analysis, including `Year`, `Month Name`, `Day of Week`, and a sortable `Year-Week` key (`YYYY-Www`).
- **Categorical Binning:** The numerical `CustomerScore` column was binned into descriptive categories (e.g., "Poor", "Fair", "Good", "Excellent") to allow for easier segmentation and comparison.

### Data Analysis & Key Findings

The analysis of the dataset uncovered several crucial insights into the bank's performance and customer behavior.

- **The Net Outflow Problem:** The most critical financial finding was that despite a high **Gross Transaction Value of $101.01 Million**, the bank had a **Net Transaction Value (Net Flow) of negative $67.36 Million**. This indicates that more money is leaving the bank through withdrawals and payments than is coming in through deposits.

- **The Middle-Income Engine:** The **`Middle Income Segment`** was identified as the bank's most valuable customer group. They lead in every key metric: total transaction value ($45.52M), total transaction volume (8,885), and total fee generation.

- **The Channel Equilibrium Paradox:** Contrary to modern banking trends where digital channels dominate, customer activity was almost perfectly distributed across all four channels: **Mobile (26.1%)**, **Branch (25.17%)**, **ATM (24.42%)**, and **Online (24.33%)**. This suggests a lack of a compelling digital-first option for customers.

- **Fee Revenue Structure:** Analysis revealed that **Late Payment Fees** are the single largest source of fee revenue across all customer segments, indicating a reliance on penalty-based income rather than value-added services.

- **Localized Seasonality:** While a global seasonal trend exists, deep dives into top-performing branches revealed unique local patterns. For example, **Barcelona**'s transaction value peaked in **January**, while **Valencia's** peaked in **March**—both different from the overall peak in April.

### Visualizations

The Power BI dashboard features a range of visuals designed to explore these findings, including:
- **KPI Dashboard:** A dedicated page for at-a-glance metrics like `Net Flow`, `Total Customers`, `Total Fee Revenue`, and dynamic measures like `Best Performing Branch`.
- **Combo Charts:** To compare Transaction Value vs. Volume for each Customer Segment.
- **Map Visual:** To identify geographic transaction hotspots by branch location.
- **Waterfall Chart:** To break down the composition of Total Fee Revenue by its sources.
- **Matrix Visual:** To analyze the effectiveness of `RecommendedOffer`s against actual `ProductCategory` usage.

### Actionable Recommendations

The analysis led to a multi-faceted strategic action plan:
1.  **Launch a Deposit Growth Initiative:** To combat the significant net outflow, introduce products and loyalty programs designed to attract and retain customer deposits.
2.  **Develop a "Middle-Income Excellence Program":** Create tailored products, services, and rewards for the bank's most valuable and engaged customer segment.
3.  **Drive Digital Channel Adoption:** Invest in the UX/UI and feature set of the mobile and online platforms to shift volume from less efficient traditional channels.
4.  **Rebalance the Fee Model:** Pivot from a reliance on penalty fees by introducing value-added services and proactively helping customers avoid late payments.
5.  **Implement Localized Marketing Calendars:** Empower key branches to launch campaigns that align with their unique seasonal peaks rather than a one-size-fits-all national calendar.

---
