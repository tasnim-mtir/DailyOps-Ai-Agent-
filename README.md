---

# 🌐 **DailyOps – AI Operations Control Agent**

### *Built with IBM watsonx Orchestrate · Vercel Frontend Deployment*

---

## 🚀 Overview

**DailyOps** is an AI-powered operations assistant that automates your morning routine by generating a **decision-ready daily briefing** based on your emails, meetings, and tasks.

It uses **IBM watsonx Orchestrate** to fetch operational data, apply intelligent prioritization rules, and return:

* 📧 Today’s most important emails
* 📅 Meetings sorted chronologically
* 📝 High-priority and overdue tasks
* ⚡ A fully optimized daily schedule
* 🔔 Blockers, risks, deadlines
* 🎤 Optional voice mode (IBM Cloud only)

The project includes:

* A **public web UI** → deployed on **Vercel**
* A **DailyOps Agent** → built inside **IBM Orchestrate**
* Full workflow orchestration using GetEmails / GetMeetings / GetTasks tools

---

## 📸 Demo

### 🔵 Live Website (Vercel)

**➡ [https://daily-ops-ai-agent.vercel.app/](https://daily-ops-ai-agent.vercel.app/)**

### 🟦 IBM Orchestrate Chat Demo

Available only through IBM Cloud (voice mode + documentation chat).

---

## ✨ Features

### 🔹 Daily Briefing Engine

Summarizes today's emails, meetings, and tasks into one clear overview.

### 🔹 Smart Prioritization

Categorizes items as **Critical / High / Normal** using advanced filtering logic.

### 🔹 Optimized Daily Schedule

Creates a timeline including:

* Buffers
* Task grouping
* Conflict detection
* Workload balancing

### 🔹 Voice Interaction (IBM Only)

Supports STT/TTS through Watson Speech services.
*Not available on public website embed.*

### 🔹 Chat with Documentation (IBM Only)

Upload files → DailyOps summarizes content for actionable insights.

### 🔹 Clean Public Web Interface

Landing page + chat route with embedded Orchestrate widget.

---

## 🏗 Architecture

```
Vercel Frontend  →  IBM Orchestrate Loader Widget  →  DailyOps Agent (LLM)

DailyOps Agent → Tools:
   ├── GetEmails
   ├── GetMeetings
   └── GetTasks
```

Agent logic includes:

* Trigger-based tool execution
* Email/meeting/task filtering
* Schedule optimization engine
* Prioritization rules
* Output formatting rules

---

## 🧱 Tech Stack

| Component | Technology                           |
| --------- | ------------------------------------ |
| Frontend  | HTML, CSS, Vercel Hosting            |
| Agent     | IBM watsonx Orchestrate              |
| LLM       | LLaMA-3-90B                          |
| Voice     | IBM Speech-to-Text & Text-to-Speech  |
| Tools     | GetEmails, GetMeetings, GetTasks     |
| Storage   | Fake demo dataset (for presentation) |

---

## 📁 Project Structure

```
/DailyOps Front
 ├── index.html           (Landing Page)
 ├── chat.html            (Embedded Orchestrate Chat)
 ├── documentation.html   (Project Documentation)
 ├── logo.png             (Brand logo)
 └── README.md
```

---

## 🔧 Installation & Local Development

1. Clone the repository:

```bash
git clone https://github.com/yourusername/DailyOps.git
```

2. Open the project folder:

```bash
cd DailyOps
```

3. Open the project locally:

* Using VSCode Live Server
* Or via browser (`index.html`)
* Or by deploying to Vercel / Netlify

*No backend required — these are static files.*

---

## 🧠 DailyOps Agent Logic (IBM Orchestrate)

### 🟦 Start-of-Day Workflow

Trigger phrases:

* “Start my day”
* “Daily briefing”
* “What do I have today?”

Tool order:

1. GetEmails
2. GetMeetings
3. GetTasks

### 🟨 Schedule Optimization Workflow

Trigger phrases:

* “Optimize my schedule”
* “Plan my day”

Tool order:

1. GetMeetings
2. GetTasks
3. GetEmails

### 🟥 Filtering Logic

* Only items **dated today**
* Ignore noise / newsletters
* Max **7 emails**, **10 tasks**
* Prioritize urgent keywords
* Sort meetings chronologically

### 🟩 Output Format

DailyOps returns:

* Email summary
* Today’s meeting list
* Task breakdown
* Top 5 priorities
* Optimized timeline
* Risks / blockers / postponements

---

## 🎤 Voice Mode (IBM Exclusive)

Voice features include:

* Real-time STT
* TTS responses
* Voice activity detection
* Interruption handling

⚠️ **Voice only works inside IBM Cloud**
It is **not supported** in the embedded chat on the website.

---

## 📘 Chat With Documentation (IBM Exclusive)

Users can upload files and DailyOps will:

* Summarize documents
* Extract action points
* Identify tasks from text
* Incorporate content into daily planning

⚠️ Not supported on Vercel frontend (IBM-only feature).

---

## 🧪 Demo Dataset

The project includes realistic fake data for:

* Emails
* Meetings
* Tasks

Used to simulate realistic operational workloads during judging demonstrations.

---

## 📈 Roadmap

* Gmail / Outlook connectors
* Real Google Calendar sync
* Multi-user workspace
* Notifications + reminders
* Dashboard for analytics
* Team assistant collaboration

---

## 🙌 Acknowledgements

This project was built for the **IBM watsonx Orchestrate Agentic AI Hackathon 2025**.

Special thanks to:

* IBM watsonx Orchestrate Team
* Event mentors and organizers

---

## 👤 Author

**Tasnim Mtir and Razi Ammari**

---

