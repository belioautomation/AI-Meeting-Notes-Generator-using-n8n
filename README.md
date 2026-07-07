# AI Meeting Notes Generator using n8n

An AI-powered meeting documentation workflow built with **n8n** and **Google Gemini AI**. This automation monitors a Google Drive folder for newly uploaded meeting transcripts, extracts the document text, generates an AI summary, identifies participants, action items, and decisions, stores the results in Google Sheets, and sends meeting summaries to Telegram.

---

## 📌 Features

- 📂 Monitors a Google Drive folder for new meeting transcripts
- 📄 Extracts text from PDF, DOCX, and TXT files
- 🤖 Uses Google Gemini AI to summarize meeting content
- 📋 Extracts structured meeting information
- 📊 Logs meeting records into Google Sheets
- 📲 Sends meeting summaries to Telegram
- ⚡ Built with Basic LLM + Information Extractor (No AI Agent)

---

## 🛠 Workflow

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

## 🚀 Technologies Used

- n8n
- Google Drive API
- Google Gemini API
- Google Sheets API
- Telegram Bot API

---

## 📦 Nodes Used

1. Google Drive Trigger
2. Download File
3. Extract From File
4. Google Gemini Chat Model
5. Information Extractor
6. Google Sheets
7. Telegram

---

## 🧠 Information Extracted

The workflow automatically extracts:

- Meeting Title
- Meeting Date
- Summary
- Participants
- Action Items
- Decisions

---

## 📱 Sample Telegram Output

```
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

## 📊 Sample Google Sheets Output

| Meeting | Date | Summary | Participants | Action Items | Decisions |
|----------|------|----------|--------------|--------------|-----------|
| Weekly Team Meeting | 2026-07-07 | Team reviewed automation roadmap and assigned responsibilities. | Belio, John, Sarah, Michael | Build workflow, Review repository, Test workflow, Deploy n8n | Continue Day 12 project |

---

## ⚙ Prerequisites

Before importing the workflow, configure the following credentials in **n8n**:

- Google Drive
- Google Gemini API
- Google Sheets
- Telegram Bot

---

## 📂 Google Drive Folder

Create a folder named:

```
Meeting Transcripts
```

Upload your meeting transcript files (PDF, DOCX, or TXT) into this folder to trigger the workflow.

---

## 📄 Google Sheets Columns

Create a spreadsheet with the following columns:

| Meeting | Date | Summary | Participants | Action Items | Decisions |
|----------|------|----------|--------------|--------------|-----------|

---

## 📁 Repository Structure

```
AI-Meeting-Notes-Generator-using-n8n
│
├── workflow.json
├── README.md
├── screenshots/
│   ├── workflow.png
│   ├── execution.png
│   ├── google-sheets.png
│   └── telegram-output.png
│
└── sample-files/
    └── Weekly_Team_Meeting_Transcript.pdf
```

---

## 🎯 Skills Demonstrated

- AI Workflow Automation
- Google Drive Integration
- Document Processing
- AI Text Summarization
- Structured Information Extraction
- Google Sheets Automation
- Telegram Notifications
- JSON Processing
- No-Code / Low-Code Development

---

## 🔮 Future Improvements

- Support multiple languages
- Export meeting summaries to Notion
- Email meeting summaries automatically
- Generate meeting action deadlines
- Support Zoom and Microsoft Teams transcripts
- Save meeting history to a database

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 👨‍💻 Author

**Belio Sinangote**

**30-Day n8n Automation Roadmap — Day 12 Project**

Building one portfolio-ready automation every day to master **n8n**, **AI Automation**, and **Workflow Development**.
