# Salesforce End-to-End Project Management Solution

A complete, enterprise-grade project management application built natively on Salesforce Core (Lightning Experience). This solution automates post-sale project onboarding, enforces data governance, streamlines record creation via Screen Flows, implements an enterprise security model, and delivers real-time executive analytics.

---

## 🚀 Key Highlights & Capabilities
* **Relational Data Architecture:** Custom Object (`Project__c`) linked via Lookup relationship to standard `Account` records.
* **Declarative Process Automation:**
  * **Screen Flow Wizard:** Context-aware quick create modal embedded on Account record pages, automatically injecting parent `recordId`.
  * **Record-Triggered Automation:** Event-driven Flow instantly instantiating priority Kickoff tasks upon lifecycle status progression (`In Progress`).
* **Data Integrity & Governance:** Validation Rule enforcing mandatory completion audit dates (`End_Date__c`) prior to marking records as `Completed`.
* **Enterprise Security & Access Model:**
  * Organization-Wide Defaults (OWD) set to **Private** to ensure least-privilege baseline.
  * Custom **Permission Set** (`Project Management Operations`) granting granular Object-level (Create, Read, Edit) and Field-Level Security (FLS).
  * **Criteria-Based Sharing Rule** automatically granting read-only visibility across all internal users when projects transition to `In Progress`.
  * Multi-persona validation verified via dedicated test user execution (`Test Operator`).
* **Executive Business Intelligence:** Summary reports grouped by lifecycle status and interactive Lightning Dashboard with KPI scorecards and status distribution charts.

---

## 📦 Architecture & Metadata Components
* **Objects & Fields:** `Project__c` schema definition, custom fields (`Status__c`, `End_Date__c`, `Account__c`), and validation logic.
* **Security & Access:** `Project_Management_Operations` Permission Set, Org-Wide Defaults, and Sharing Rules.
* **Automation (Flows):** `Project_Quick_Create_Wizard` (Screen Flow) and `Project_Create_Kickoff_Task_on_In_Progress` (Record-Triggered Flow).
* **UI/UX:** Custom Lightning Record Page with segregated Activity Timeline layout.
* **Analytics:** Pre-configured public Report and Dashboard folders.

---

## 🛠️ Installation & Documentation
* **Direct Package Installation URL:** [Install Package in Salesforce Org](https://login.salesforce.com/packaging/installPackage.apexp?p0=04tgK000000Js6L&isdtp=p1)
* **Architecture Documentation:** Review the attached `Salesforce_Project_Management_Solution_Design.pdf` for full architecture specifications, data dictionary, and validation matrices.
