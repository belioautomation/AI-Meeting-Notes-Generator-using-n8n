# 📝 AI Meeting Notes Generator — n8n Automation

![n8n](https://img.shields.io/badge/n8n-Automation-orange)
![Google Gemini](https://img.shields.io/badge/AI-Google%20Gemini-blue)
![Google Drive](https://img.shields.io/badge/Storage-Google%20Drive-green)
![JavaScript](https://img.shields.io/badge/Code-JavaScript-yellow)
![License](https://img.shields.io/badge/license-MIT-green)

An AI-powered meeting documentation workflow built using **n8n**, **Google Drive API**, **Google Gemini AI**, **Google Sheets**, and **Telegram Bot API**.

This system automatically monitors a Google Drive folder for newly uploaded meeting transcripts, extracts document content, analyzes meeting discussions using AI, generates structured meeting notes, identifies participants, action items, and important decisions, stores results in Google Sheets, and sends instant summaries through Telegram.

**Stack:**  
n8n · Google Drive API · Google Gemini AI · Google Sheets · Telegram Bot · JavaScript · AI Automation


---

# 🎯 Project Overview


## Problem

Managing meeting documentation manually creates several challenges:

- Time-consuming note-taking
- Important decisions can be forgotten
- Difficult tracking of assigned tasks
- Manual creation of meeting summaries
- Poor organization of meeting records


Common scenarios:

- Team meetings
- Project discussions
- Client meetings
- Sprint planning sessions
- Business reviews


---

## Solution

This project creates an automated AI meeting documentation system by:


1. Monitoring Google Drive for new meeting transcripts
2. Downloading uploaded documents automatically
3. Extracting text from meeting files
4. Analyzing content using Google Gemini AI
5. Generating structured meeting notes
6. Extracting participants, action items, and decisions
7. Saving results into Google Sheets
8. Sending summaries through Telegram


The workflow acts as an AI meeting assistant that transforms raw transcripts into organized and actionable documentation.


---

# ✨ Features


## Document Processing

✅ Automatic Google Drive monitoring  
✅ New transcript detection  
✅ PDF, DOCX, and TXT support  
✅ Automated text extraction  


## Artificial Intelligence

✅ Google Gemini AI analysis  
✅ AI-generated meeting summaries  
✅ Participant identification  
✅ Action item extraction  
✅ Decision extraction  
✅ Structured information output  


## Data Management

✅ Google Sheets meeting database  
✅ Organized meeting records  
✅ Automatic documentation storage  
✅ Structured meeting information  


## Notifications

✅ Telegram instant summaries  
✅ Real-time workflow updates  
✅ Automated meeting documentation delivery  


---

# 🗺️ System Architecture


```mermaid
flowchart TD

A["📂 Google Drive Folder"]

--> B["📥 Google Drive Trigger"]


B --> C["⬇️ Download File"]


C --> D["📄 Extract From File"]


D --> E["🤖 Google Gemini AI"]


E --> F["📋 Information Extractor"]


F --> G["📊 Google Sheets Database"]


G --> H["📱 Telegram Notification"]

````

---

# 🏗️ Workflow Implementation

# Workflow 1: AI Meeting Documentation Pipeline

## Node 1 — Google Drive Trigger

### Purpose

Monitor a specific Google Drive folder for newly uploaded meeting transcripts.

Configuration:

```text
Event:

File Created


Folder:

Meeting Transcripts
```

Captured Information:

| Field        | Description              |
| ------------ | ------------------------ |
| File Name    | Uploaded transcript name |
| File ID      | Google Drive identifier  |
| File Type    | Document format          |
| Created Date | Upload timestamp         |

---

# Node 2 — Download File

### Purpose

Retrieve the uploaded transcript file from Google Drive for processing.

Supported Formats:

```text
PDF

DOCX

TXT
```

Processing:

```text
Google Drive File

        ↓

Downloaded Document

        ↓

Text Extraction
```

---

# Node 3 — Extract From File

### Purpose

Convert uploaded documents into readable text data.

Extracted Information:

| Field            | Description          |
| ---------------- | -------------------- |
| Transcript Text  | Meeting conversation |
| Document Content | Raw extracted text   |

Example:

```text
Meeting Transcript:

John:
Today we will review project progress.

Belio:
The automation workflow is completed.
```

---

# Node 4 — Google Gemini Chat Model

### Purpose

Analyze the meeting transcript and generate intelligent meeting documentation.

The AI extracts:

* Meeting summary
* Main discussion points
* Participants
* Action items
* Decisions

Example Response:

```json
{
"summary":
"Team reviewed automation progress and upcoming tasks.",

"participants":
[
"Belio",
"John",
"Sarah"
],

"action_items":
[
"Update workflow documentation"
],

"decisions":
[
"Continue using Google Gemini AI"
]
}
```

---

# Node 5 — Information Extractor

### Purpose

Convert AI output into structured meeting information.

Extracted Fields:

| Field         | Description           |
| ------------- | --------------------- |
| Meeting Title | Meeting name          |
| Date          | Meeting date          |
| Summary       | AI-generated overview |
| Participants  | People involved       |
| Action Items  | Assigned tasks        |
| Decisions     | Final agreements      |

---

# Node 6 — Google Sheets

### Purpose

Store generated meeting notes for documentation and future reference.

Database Structure:

| Field        | Description     |
| ------------ | --------------- |
| Meeting      | Meeting title   |
| Date         | Meeting date    |
| Summary      | AI summary      |
| Participants | Attendees       |
| Action Items | Assigned tasks  |
| Decisions    | Final decisions |

Example:

| Meeting             | Date       | Summary                        |
| ------------------- | ---------- | ------------------------------ |
| Weekly Team Meeting | 2026-07-07 | Automation progress discussion |

---

# Node 7 — Telegram Notification

### Purpose

Send AI-generated meeting summaries instantly.

Example:

```text
📋 AI Meeting Notes


📝 Meeting:

Weekly Team Meeting


📅 Date:

2026-07-07


👥 Participants:

Belio, John, Sarah


📌 Summary:

The team reviewed automation projects and discussed upcoming development tasks.


✅ Action Items:

• Belio - Update workflow documentation

• John - Review repository


🎯 Decisions:

• Continue using Google Gemini AI
```

---

# 🔐 Credentials Required

| Service              | Purpose                    |
| -------------------- | -------------------------- |
| Google Drive OAuth2  | Monitor and download files |
| Google Gemini API    | AI analysis                |
| Google Sheets OAuth2 | Store meeting records      |
| Telegram Bot API     | Send notifications         |
| n8n Instance         | Workflow execution         |

---

# ⚙️ Setup Guide

## 1. Configure Google Drive Trigger

Create Google Drive OAuth credentials.

Required:

```text
Google Account

Drive API Access

Folder Permission
```

Test file upload detection.

---

## 2. Configure Google Gemini AI

Create Gemini API credentials.

Required:

```text
Google AI API Key

Gemini Model Access
```

Test transcript analysis.

---

## 3. Create Google Sheets Database

Create:

```text
AI Meeting Notes Database
```

Columns:

```text
Meeting

Date

Summary

Participants

Action Items

Decisions
```

---

## 4. Configure Telegram Bot

Steps:

1. Create Telegram bot using BotFather
2. Copy bot token
3. Add Telegram credential in n8n
4. Configure chat ID

---

## 5. Import Workflow

Import:

```text
workflow.json
```

Configure:

* Google Drive Trigger
* Gemini API
* Google Sheets
* Telegram

Activate workflow.

---

# 🧪 Testing Checklist

| Test Case                  | Expected Result          |
| -------------------------- | ------------------------ |
| Upload transcript file     | Workflow starts          |
| File downloaded            | Document retrieved       |
| Text extraction runs       | Transcript converted     |
| Gemini analyzes content    | Summary generated        |
| Information Extractor runs | Structured notes created |
| Google Sheets updates      | Meeting saved            |
| Telegram sends message     | Summary received         |

---

# 📁 Repository Structure

```text
AI-Meeting-Notes-Generator-n8n/

│
├── README.md
│
├── workflow.json
│
├── screenshots/
│
│   ├── workflow.png
│   ├── google-drive-trigger.png
│   ├── extract-file.png
│   ├── gemini-output.png
│   ├── information-extractor.png
│   ├── google-sheets.png
│   ├── telegram-notification.png
│   └── execution-result.png
│
└── LICENSE
```

---

# 📸 Screenshots

Recommended screenshots:

* Complete workflow
* Google Drive Trigger configuration
* Extract From File output
* Gemini AI response
* Information Extractor output
* Google Sheets records
* Telegram notification
* Workflow execution result

---

# 🚀 Future Improvements

| Feature                 | Implementation               |
| ----------------------- | ---------------------------- |
| Notion Integration      | Store meeting knowledge base |
| Email Delivery          | Send summaries automatically |
| Calendar Integration    | Link meetings with schedules |
| Deadline Detection      | Generate task deadlines      |
| Multi-language Support  | Translate meeting notes      |
| Zoom Integration        | Process recorded meetings    |
| Microsoft Teams Support | Import Teams transcripts     |
| Dashboard Analytics     | Meeting insights dashboard   |

---

# 🎓 Skills Applied

## Automation

* n8n Workflow Automation
* Event-driven workflows
* Document processing pipelines

## Artificial Intelligence

* Google Gemini API
* Prompt Engineering
* AI summarization
* Information extraction

## APIs

* Google Drive API
* Google Sheets API
* Telegram Bot API

## Programming

* JavaScript
* JSON processing
* Data transformation
* Workflow logic

## Business Automation

* Meeting documentation
* Productivity automation
* AI-powered knowledge management

---

# 📚 Learning Objectives

This project demonstrates:

* Building AI-powered document workflows
* Automating meeting documentation
* Integrating cloud storage with AI
* Extracting structured information from text
* Creating productivity automation systems

---

# 🙌 Acknowledgements

* n8n
* Google Gemini AI
* Google Drive API
* Google Sheets API
* Telegram Bot API

---

# 👨‍💻 Author

**Belio C. Sinangote**

BS Information Technology Student
Cebu Technological University (CTU)

GitHub:

[https://github.com/belioautomation](https://github.com/belioautomation)

This project is part of my **30-Day n8n Automation Portfolio**, showcasing practical automation solutions using **n8n, AI integrations, APIs, and business workflow automation**.

---

# 📄 License

MIT License

```
```
