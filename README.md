# End-to-End Lead Management & Sales Performance Analytics

## 🎯 Project Overview & Business Value
In fast-paced corporate sales environments, data fragmentation stalls deals and creates blind spots for leadership. This project showcases the end-to-end development of an enterprise-grade **Sales Overview Dashboard** designed to eliminate pipeline visibility gaps. By transforming and consolidating disconnected operational tracking systems, this business intelligence asset provides executive stakeholders with real-time, actionable insights into lead stagnation, pipeline funnel velocity, and sales executive performance.

* **Key Deliverable:** Interactive executive dashboard tracking the real-time health of 389 concurrent corporate accounts.
* **Target Impact:** Optimized follow-up frequencies, isolated operational bottlenecks, and automated revenue pipeline auditing.

---

## 🛠️ The Data Engineering Challenge (The 9-Day ETL Marathon)
*This section demonstrates your ability to wrestle with real-world, unhygienic corporate data structures rather than idealized classroom datasets—a key differentiator for high-paying roles.*

### 1. The Core Infrastructure Problem
The organization's legacy Sales ERP system was highly decentralized, storing transactional data across **12+ separate spreadsheet trackers**, each exceeding 1,000 rows of unformatted logs. Data fields suffered from inconsistent schemas, high-volume missing category values, unstandardized stage naming conventions, and conflicting lead entry timelines. 

### 2. Data Transformation & Pipeline Strategy
Over a rigorous **9-day data engineering pipeline process**, I executed a comprehensive Extraction, Transformation, and Loading (ETL) workflow to unify this fragmented ecosystem into a singular, clean relational fact table (`NBD Leads Stage Github.csv`):
* **Schema Standardization & Consolidation:** Aligned and appended multi-sheet horizontal architectures into a unified, vertical schema.
* **Imputation & Missing Value Architecture:** Addressed high-volume null fields (specifically in categorical tracking columns) by establishing consistent logical defaults (e.g., mapping undefined categories to standard fallback classes).
* **Feature Engineering (Stagnation Tracking):** Engineered dynamic data logic to compute the `Inactive Days` and `Average Inactive Days` metrics, laying the analytical foundation for the aging analysis engine.
* **Enterprise Anonymization & Data Security:** Masked all proprietary B2B client details, corporate trade secrets, and employee identifiers with randomized corporate taxonomy tokens to ensure public repository safety without altering operational data distribution patterns.

---

## 📊 Analytics Architecture & Dashboard Blueprint
The dashboard follows an intentional, top-down UI/UX reporting framework designed for fast executive decision-making.

![Sales Dashboard](https://github.com/ranvirsingh603/Sales-Overview-Dashboard/blob/main/Sales%20Overview%20Dashboard%20Screenshot.png)

### 1. Executive Headline KPIs
* **Total Volume Hub:** Real-time visibility into the complete active pipeline ecosystem (389 Total Leads).
* **The Stagnation Index:** An engineered metric showing an **Average Inactivity of 19.41 Days** across the company—instantly pointing to a systemic breakdown in automated follow-up cadences.
* **The High-Value Concentration Core ("Golden Leads"):** Isolates and tracks premium revenue drivers (132 Golden Leads), showing that **33.93% of the total pipeline volume** controls the vast majority of company conversion goals.

### 2. Conversions & Funnel Velocity (Middle Layer)
* **Lead Stage Funnel:** Tracks granular prospective drops. It highlights that while **Inquiry Followups (216)** and **Meeting Followups (108)** boast strong initial momentum, an acute drop-off occurs at the **Proposal to Order (39)** juncture.
* **Aging Analysis Breakdown:** Bins stagnating leads into custom operational buckets. It isolates a critical operational risk: **26 high-priority leads have been stagnant for 60+ days**, signaling immediate churn risks.

---

## 💡 Strategic Data-Driven Recommendations For Leadership
Based on the patterns uncovered by this dashboard asset, management can execute several immediate operational pivots:
1. **Targeted Account Salvage:** Deploy an elite closing team to intervene on the 26 accounts languishing in the 60+ days inactive zone before total account drop-off occurs.
2. **Standardize the Velocity Bridge:** Audit the transition between 'Meeting Followup' and 'Proposal to Order' to determine why more than 60% of verified meetings fail to generate formal purchase orders.
3. **Reallocate Sales Workload:** Optimize human capital distribution by re-assigning unmanaged accounts or balancing high-volume pipelines among under-utilized Sales Executives.

---

## 📂 Project Repository Directory

```text
├── Leads Stage.csv
│   └── Unified, anonymized relational source table (389 rows)
│
├── Sales Overview Dashboard.pbix
│   └── Production-ready Power BI Desktop file
│
├── Sales Overview Dashboard Screenshot.jpg
│   └── Full-resolution dashboard interface screenshot
│
└── README.md
    └── Project documentation & case study
```

---

## ⚙️ Local Deployment & Replication Instructions

To interact with or review the engineering mechanics behind this business intelligence file:

1. Download or clone this repository to your local workspace.
2. Download both the `.pbix` file and the source `.csv` file.
3. Open the `.pbix` file using Power BI Desktop.
4. Resolve Data Source Paths:

   * If a local file path error displays, navigate to:
     `Home → Transform Data → Data Source Settings`
   * Select **Change Source**
   * Re-point the file path to your local copy of:
     `NBD Leads Stage Github.csv`
