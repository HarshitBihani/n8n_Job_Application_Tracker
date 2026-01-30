<img width="355" height="142" alt="download" src="https://github.com/user-attachments/assets/1ffc3fa1-f4c5-4d65-9b67-d6b5cd3e08a5" />


# Job Application Tracker (n8n)

An **end-to-end automated job tracking system** built using **n8n**, designed to **collect, normalize, deduplicate, store, and notify** job opportunities from multiple sources all without manual effort.

This workflow continuously scans job platforms, parses listings, removes duplicates, saves them into Google Sheets, and sends email summaries
.

---

##  What This Workflow Does

This n8n workflow automatically:

- 🔍 Searches for jobs based on configured criteria  
- 🌐 Scrapes jobs from multiple platforms (LinkedIn, Indeed, Remote APIs)  
- 🧠 Normalizes & merges data from different sources  
- 🧹 Removes duplicate job postings  
- 📊 Stores structured job data in Google Sheets  
- ✉️ Sends email summaries of new job listings  
- ⏰ Runs automatically on a fixed schedule  

---

## 🧠 System Architecture

```text
Scheduled Trigger
        ↓
Search Configuration
        ↓
Job Sources
(LinkedIn | Indeed | Remote APIs)
        ↓
Parsing & Normalization
        ↓
Merge All Sources
        ↓
Duplicate Removal
        ↓
Filtering Logic
        ↓
Google Sheets (Job Tracker)
        ↓
Email Summary Notification
```


## Workflow Overview

### ⏰ Scheduled Execution
- Triggered automatically **every few hours**
- Ensures fresh and up-to-date job listings

---

### 🔍 Job Data Collection
Pulls jobs from:
- LinkedIn scraping
- Indeed scraping
- Remote job APIs  

Each source has its **own parsing logic**

---

### 🧠 Data Processing
Standardizes fields such as:
- Job Title
- Company Name
- Location
- Job URL
- Source Platform  

Merges all job data into a **single unified stream**

---

### 🧹 Duplicate Handling
Removes repeated job listings using:
- Job URL
- Title + Company combination  

Ensures **clean and unique records**

---

### 📊 Google Sheets Integration
Automatically:
- Appends new jobs
- Updates existing records (if required)  

Acts as a **live job application tracker**

---

### ✉️ Email Notifications
- Generates a concise email summary
- Sends newly found jobs directly to your inbox
- Helps you apply faster without checking sheets manually

---

## 📊 Google Sheets as Dashboard

Your Google Sheet becomes a **live job dashboard**, tracking:
- Job title
- Company
- Location (Remote / Onsite / Hybrid)
- Job source
- Application status
- Notes / follow-ups  

Perfect for:
- Daily job hunting
- Application tracking
- Follow-up management

---

## 🛠️ Tech Stack Used

- **n8n** – Workflow automation engine  
- **HTTP Request / Scraper Nodes** – Job data collection  
- **JavaScript (n8n expressions)** – Parsing & transformations  
- **Merge Node** – Combining multiple job sources  
- **Filter & Deduplication Logic** – Data hygiene  
- **Google Sheets API** – Persistent job tracking  
- **Gmail Node** – Automated email notifications  

---

## ⚙️ Setup Instructions

### 1️⃣ Prerequisites
- n8n installed (Local / Docker / Cloud)
- Google account with access to Google Sheets
- Gmail account for email notifications

---

### 2️⃣ Import Workflow
- Open n8n  
- Click **Import Workflow**  
- Import the workflow JSON  
- Save the workflow  

---

### 3️⃣ Configure Search Criteria
- Open **Configure Search** node  
- Define:
  - Job roles
  - Keywords
  - Locations
  - Experience level

---

### 4️⃣ Configure Credentials
- Add **Google Sheets OAuth** credentials  
- Add **Gmail OAuth** credentials  
- Update Spreadsheet ID and Sheet Name  

---

### 5️⃣ Activate Workflow
- Activate the workflow  

Jobs will now be:
- Fetched automatically
- Stored in Google Sheets
- Sent via email summaries

---

## 💡 Use Cases

- Students & freshers tracking internships  
- Developers automating job hunting  
- Recruiter role monitoring   
- Scaling job search without manual effort  

