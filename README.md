# 📝 AI Meeting Notes Generator using n8n

An AI-powered meeting documentation workflow built with **n8n** and **Google Gemini AI**. This workflow automatically monitors a Google Drive folder for newly uploaded meeting transcripts, extracts the document text, generates AI-powered meeting summaries, identifies participants, action items, and key decisions, logs the results to Google Sheets, and sends meeting summaries to Telegram.

Built as part of my **30-Day n8n Automation Portfolio**, this project demonstrates document processing, AI-powered summarization, structured information extraction, and workflow automation.

---

## 📌 Features

- 📂 Monitors Google Drive for new meeting transcripts
- 📄 Extracts text from PDF, DOCX, and TXT files
- 🤖 Generates AI-powered meeting summaries using Google Gemini AI
- 📋 Extracts participants, action items, and decisions
- 📊 Logs meeting records to Google Sheets
- 📲 Sends meeting summaries via Telegram
- ⚡ Fully automated workflow

---

## 🛠️ Technologies Used

- n8n
- Google Drive Trigger
- Google Drive API
- Extract From File
- Google Gemini Chat Model
- Information Extractor
- Google Sheets API
- Telegram Bot API

---

## 📂 Workflow

```text
Google Drive Trigger
        │
        ▼
Download File
        │
        ▼
Extract From File
        │
        ▼
Google Gemini Chat Model
        │
        ▼
Information Extractor
        │
        ▼
Google Sheets
        │
        ▼
Telegram
```

---

## ⚙️ Workflow Explanation

### 1. Google Drive Trigger

Monitors a Google Drive folder for newly uploaded meeting transcripts.

Configuration:

- Event: File Created
- Folder: Meeting Transcripts

---

### 2. Download File

Downloads the uploaded transcript for processing.

Supported formats:

- PDF
- DOCX
- TXT

---

### 3. Extract From File

Extracts all text from the uploaded meeting transcript.

---

### 4. Google Gemini Chat Model

Analyzes the meeting transcript and generates an AI summary.

---

### 5. Information Extractor

Extracts structured meeting information, including:

- Meeting Title
- Meeting Date
- Summary
- Participants
- Action Items
- Decisions

---

### 6. Google Sheets

Stores all extracted meeting information for documentation and future reference.

---

### 7. Telegram

Sends an instant notification containing the meeting summary.

Example:

```text
📋 AI Meeting Notes

📝 Meeting
Weekly Team Meeting

📅 Date
2026-07-07

👥 Participants
Belio Sinangote, John Reyes, Sarah Cruz, Michael Tan

📌 Summary
The team reviewed completed automation projects, discussed the Day 12 workflow, assigned responsibilities, and agreed on the next development tasks.

✅ Action Items
• Belio – Build Day 12 workflow
• John – Review GitHub repository
• Sarah – Test workflow outputs
• Michael – Deploy updated n8n instance

🎯 Decisions
• Proceed with AI Meeting Notes Generator
• Standardize all README files
• Continue using Google Gemini Flash
```

---

## 📊 Google Sheets Structure

| Meeting | Date | Summary | Participants | Action Items | Decisions |
|----------|------|----------|--------------|--------------|-----------|

---

## 📁 Repository Structure

```text
AI-Meeting-Notes-Generator-using-n8n/
│
├── README.md
├── workflow.json
│
├── screenshots/
│   ├── workflow.png
│   ├── execution.png
│   ├── google-sheets.png
│   └── telegram-output.png
```

---

## 📷 Screenshots

Include the following screenshots:

- Complete Workflow
- Google Drive Trigger
- Extract From File
- Google Gemini Output
- Information Extractor
- Google Sheets Results
- Telegram Notification
- Workflow Execution

---

## 🎯 Learning Objectives

This project demonstrates:

- Google Drive Automation
- Document Processing
- AI Text Summarization
- Structured Information Extraction
- Google Sheets Automation
- Telegram Automation
- Workflow Automation
- AI-Powered Meeting Documentation

---

## 🚀 Future Improvements

- Support multiple languages
- Export meeting summaries to Notion
- Email meeting summaries automatically
- Generate meeting deadlines
- Support Zoom and Microsoft Teams transcripts
- Store meeting history in a database

---

## 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Belio C. Sinangote**

BS Information Technology Student  
Cebu Technological University (CTU)

**GitHub:** https://github.com/belioautomation

This project is part of my **30-Day n8n Automation Portfolio**, showcasing practical workflow automation using **n8n**, **Google Gemini AI**, and **document processing**.
