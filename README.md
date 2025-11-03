# 📞 Call Centre Performance Dashboard – Power BI

A professional Power BI project that analyzes call-centre operations and customer experience metrics. This README explains the business problem, data model, transformations, DAX measures, and how to run the report.

---

## 🔗 Repository

**Project URL:** [https://github.com/mangal-singh001/Call-Centre-Power-BI-Project-](https://github.com/mangal-singh001/Call-Centre-Power-BI-Project-)

> Tip: Keep raw data, Power Query/DAX notes, and screenshots inside this repo so anyone can reproduce the dashboard easily.

---

## 🧭 Table of Contents

* [About the Project](#about-the-project)
* [Business Questions / KPIs](#business-questions--kpis)
* [Data Sources & Structure](#data-sources--structure)
* [Data Cleaning & Transformations (Power Query)](#data-cleaning--transformations-power-query)
* [Data Model](#data-model)
* [Key DAX Measures](#key-dax-measures)
* [Report Pages & Highlights](#report-pages--highlights)
* [How to Use / Reproduce](#how-to-use--reproduce)
* [Folder Structure](#folder-structure)
* [Results & Insights](#results--insights)
* [Future Improvements](#future-improvements)
* [Screenshots](#screenshots)
* [Tech Stack](#tech-stack)
* [Author](#author)
* [License](#license)

---

## 📙 About the Project

Call centres generate high volumes of interaction and service data. This dashboard tracks operational efficiency and customer satisfaction across time, channels, regions, and agents. It helps decision-makers identify bottlenecks, improve response rates, and optimize staffing.

**What this dashboard covers:**

* Total call volume and answered vs. missed calls
* Average call duration & response time %
* First Call Resolution (FCR) & SLA compliance
* Customer sentiment & CSAT (customer satisfaction) trends
* Top call reasons & interaction channels
* Performance by agent, team, and region

---

## 🎯 Business Questions / KPIs

**Primary KPIs**

* **Total Calls**
* **Answered Calls** & **Missed Calls**
* **Response Rate %** = Answered / Total Calls
* **Average Handle Time (AHT)**
* **Average Speed of Answer (ASA)**
* **First Call Resolution (FCR) %**
* **Service Level (SLA) Compliance %**
* **Customer Satisfaction (CSAT)**
* **Repeat Call Rate %**

**Secondary Views**

* Calls by **Channel** (Phone, Chat, Email, etc.)
* Calls by **Reason/Category**
* Performance by **Region/City**
* **Peak Hours / Day-of-Week** patterns
* **Agent-level** efficiency & quality metrics

---

## 🗂️ Data Sources & Structure

* **Format:** CSV/Excel (replace if different)
* **Typical fields (example):**

  * `Call_ID`, `DateTime`, `Agent_ID`, `Agent_Name`, `Channel`, `Region`, `Call_Reason`, `Call_Duration_Seconds`, `Answered_Flag`, `First_Resolution_Flag`, `SLA_Met_Flag`, `Customer_Sentiment`, `CSAT_Score`

> If your schema differs, update this section and the DAX accordingly.

---

## 🧹 Data Cleaning & Transformations (Power Query)

1. **Data Types:** Ensure proper types for dates, durations, flags, and numeric columns.
2. **Null Handling:** Replace or remove nulls in key columns (e.g., `Answered_Flag`).
3. **Standardization:**

   * Normalize `Channel` names (e.g., PHONE/phone → "Phone").
   * Map `Customer_Sentiment` to an ordered category (Negative < Neutral < Positive).
4. **Derived Columns:**

   * **Date** (from `DateTime`)
   * **Hour** (0–23) for peak-hour analysis
   * **Call_Duration_Minutes** = `Call_Duration_Seconds / 60`
5. **Dim Tables (Optional):** Create `DimDate`, `DimAgent`, `DimRegion` for better modeling.

> Keep
