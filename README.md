

# 📧 Daily Task Digest Automation

An **n8n workflow automation** that automatically retrieves pending tasks from a Google Sheets task tracker, formats them into a clean daily summary, and emails a task digest every morning. This workflow eliminates the need for manually checking spreadsheets and ensures important tasks are never overlooked.

## 🚀 Features

* ⏰ Automatically runs every day at **8:00 AM**
* 📊 Reads task data directly from **Google Sheets**
* ✅ Filters out completed tasks
* 📝 Extracts task names and due dates
* 📋 Formats each pending task into an easy-to-read list
* 📧 Sends a daily email digest through Gmail
* 🔄 Fully automated with no manual intervention

---

## 🏗️ Workflow Architecture

```
Schedule Trigger (8:00 AM)
          │
          ▼
Read Tasks from Google Sheets
          │
          ▼
Filter Pending Tasks
          │
          ▼
Extract Required Fields
          │
          ▼
Loop Through Tasks
          │
          ▼
Format Task Entries
          │
          ▼
Build Daily Digest
          │
          ▼
Send Email via Gmail
```

---

## 🛠️ Technologies Used

* **n8n**
* **Google Sheets API**
* **Gmail OAuth2**
* **Cron Scheduler**
* **Workflow Automation**
* **Data Transformation**
* **Conditional Logic**

---

## 📂 Workflow Logic

### 1. Schedule Trigger

Runs automatically every day at **8:00 AM**.

### 2. Read Tasks

Fetches task records from a Google Sheets document.

Example data:

| Task          | Due Date | Status    |
| ------------- | -------- | --------- |
| Finish Report | June 20  | pending   |
| Submit Resume | June 21  | completed |
| Team Meeting  | June 22  | pending   |

---

### 3. Filter Pending Tasks

Removes every task whose status is **completed**, leaving only outstanding work.

---

### 4. Extract Required Fields

Keeps only the necessary information:

* Task Name
* Due Date

---

### 5. Format Each Task

Converts each task into a standardized line:

```
- Finish Report (Due: June 20)
- Team Meeting (Due: June 22)
```

---

### 6. Build Daily Digest

Combines all formatted tasks into a single email body.

Example output:

```
Daily Task Digest - June 20, 2025

- Finish Report (Due: June 20)
- Team Meeting (Due: June 22)

Total pending tasks: 2
```

---

### 7. Send Email

Automatically delivers the digest using Gmail.

**Subject**

```
Daily Task Digest - June 20, 2025
```

---

## 📈 Benefits

* Eliminates repetitive manual task checking
* Centralizes pending tasks into a single daily email
* Improves personal productivity and task visibility
* Demonstrates practical business process automation using low-code workflows
* Can be easily extended for team-wide reporting or project management

---

## 🔮 Possible Enhancements

* Priority-based task sorting
* Color-coded email formatting (HTML)
* Slack or Microsoft Teams notifications
* Overdue task highlighting
* Multiple recipients
* Calendar integration
* AI-generated task summaries
* Dynamic filtering by assignee or project
* Dashboard integration with Power BI or Looker Studio

---

## 📸 Workflow Overview

Import the provided `Daily Task Digest Automation.json` file into n8n to view and execute the complete workflow.

---

## 💼 Skills Demonstrated

* Workflow Automation
* Business Process Automation
* Google Sheets API Integration
* Gmail API Integration
* OAuth2 Authentication
* Data Extraction & Transformation
* Conditional Logic
* Scheduled Workflows (Cron)
* Low-Code Automation
* Process Optimization
* Productivity Automation
* ETL Concepts

---

This project demonstrates how **n8n** can automate repetitive reporting workflows by integrating Google Workspace services, transforming spreadsheet data into actionable insights, and delivering scheduled notifications with minimal maintenance. It showcases practical skills in workflow orchestration, API integration, and business process automation that are commonly used in operations, analytics, and productivity engineering roles.
