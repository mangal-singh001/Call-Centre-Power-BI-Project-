# 📞 Call Centre Performance Dashboard – Power BI

A professional **Power BI dashboard** to analyze call-centre performance and customer experience.
This project helps understand agent productivity, call trends, customer sentiment, and service efficiency to support better decision-making.

---

## 🎯 Project Overview

Call centers handle thousands of interactions daily. To ensure efficiency and customer satisfaction, it’s essential to monitor:
✅ Call volume trends
✅ Agent performance
✅ Customer sentiment & satisfaction
✅ Resolution rates & SLA compliance
✅ Peak call hours & channel insights

This dashboard answers all of the above through clean visuals and KPI tracking.

---

## 📸 Dashboard Preview  
![Call Centre Dashboard](Dashboard.png)

---

## 📂 Dataset

* **Source**: Call Center dataset (CSV)
* **File**: `Call Center_Call Center.csv`
* **Tool Used**: Power BI Desktop

---

## 🔧 Data Cleaning & Preparation

🧼 Handled missing values & inconsistent formats
🕒 Extracted date & hour from datetime
🎭 Standardized call types & sentiment categories
🔗 Built fact-to-dimension relationships
📐 Created calculated columns for time & performance metrics

---

## 💡 Key Metrics & DAX Measures

| Metric                               | Description                     |
| ------------------------------------ | ------------------------------- |
| 📞 **Total Calls**                   | Total number of calls received  |
| 📈 **Answered Calls%**               | % of calls successfully handled |
| 📉 **Missed Calls**                  | Calls not answered              |
| ⏳ **Average Handle Time (AHT)**      | Average call duration           |
| ⚡ **Service Level %**                | Calls answered under SLA        |
| 😊 **CSAT**                          | Customer satisfaction score     |
| 🎯 **First Call Resolution % (FCR)** | Issues resolved on first call   |

**Sample DAX**

```DAX
Total Calls = COUNTROWS(Calls)

Answered Calls = CALCULATE([Total Calls], Calls[Answered_Flag] = TRUE())

Response Rate % = DIVIDE([Answered Calls], [Total Calls], 0)
```

---

## 📊 Dashboard Highlights

✨ KPI Cards (Calls, SLA, CSAT, FCR)
📈 Trend analytics (daily/weekly/monthly)
🌎 Regional performance charts
🎧 Agent leaderboard
💬 Customer sentiment visualization
⏱ Peak hour analysis

---

## 🧠 Insights

* 🚀 **High call traffic** observed between **10 AM – 12 PM**
* 😟 Slight dip in **CSAT during peak hours**
* 🎤 Certain agents show **higher call resolution efficiency**
* 🔁 A few call categories show **repeat customer queries → improvement area**

*(Update these based on your final findings)*

---

## 📁 Folder Structure

```
📁 repository
 ┣ 📄 Call Centre.pbix
 ┣ 📄 Call Center_Call Center.csv
 ┣ 🖼 Dashboard Screenshot (optional)
 ┗ 📄 README.md
```

---

## 🛠 Tech Stack

| Tool        | Purpose                   |
| ----------- | ------------------------- |
| Power BI    | Visualization & reporting |
| Power Query | Data cleaning             |
| DAX         | Calculation measures      |
| CSV         | Data source               |

---

## 🚀 Future Enhancements

* Real-time call monitoring using API
* AI-based sentiment analysis from transcripts
* Forecast call volume using ML
* Automated alert system for SLA breach

---

## 👤 Author

**Mangal Singh**
🌐 GitHub: **github.com/mangal-singh001**
🔗 LinkedIn: **https://www.linkedin.com/in/mangal-singh123/**

---

## ⭐ Support

If you like this project, please give it a ⭐ on GitHub!

---
