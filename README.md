# AI-Enabled Meeting Notes & Weekly Highlights Automation

## Overview
This project demonstrates an AI-powered automation system that captures meeting notes and key business updates through a web interface built using Lovable and processes them using n8n workflows.

The system supports two parallel automation flows:
1. **Weekly Highlights Automation**
2. **Instant Minutes of Meeting (MoMs) Generation**

Both workflows store structured data in Google Sheets and automate stakeholder communication through scheduled and event-based emails.

---

## Weekly Highlights Automation (Monday Summary)

### Business Use Case
Leadership often requires a consolidated view of important updates and completed tasks from the previous week. Manually tracking and summarising these updates is time-consuming and prone to omissions.

### How the Weekly Highlights Process Works

1. During the week, whenever an important task, milestone, or achievement is completed (e.g., on Tuesday or Thursday), the user opens the **Lovable web interface**.
2. The user enters the completed task details (bullet points or short description) and submits the form.
3. The **n8n workflow** captures the submission and stores it as a new entry in **Google Sheets**, along with a timestamp.
4. This process continues throughout the week, allowing multiple updates to be captured incrementally.
5. Every **Monday**, a scheduled n8n workflow automatically:
   - Fetches all entries from **the previous week** from Google Sheets
   - Compiles them into a structured weekly highlights summary
   - Generates a concise, AI-assisted narrative suitable for leadership
   - Sends a consolidated **Weekly Highlights email** to stakeholders

### Key Advantage
Important updates are captured when they happen, but communication is intentionally delayed and consolidated to ensure a clean, high-impact weekly summary.

---

## Instant MoMs (Minutes of Meeting) Automation

### Business Use Case
Meeting outcomes and action items need to be communicated immediately to avoid confusion and missed follow-ups.

### How the MoM Process Works

1. The user enters meeting notes and discussion points into the **Lovable web interface**.
2. On submission, the **n8n workflow**:
   - Structures the meeting notes
   - Stores the MoM data in **Google Sheets** for traceability
   - Generates a formatted Minutes of Meeting document using AI
3. The MoM email is **sent instantly** to meeting participants and stakeholders.

### Key Difference from Weekly Highlights
- **MoMs:** Captured and sent immediately  
- **Weekly Highlights:** Captured continuously but sent only once every Monday  

---

## Tech Stack
- Lovable – Web interface for user input
- n8n – Workflow automation and scheduling
- Google Sheets – Centralised data storage
- Large Language Models (LLMs) – Content structuring and summarisation
- Email automation – Stakeholder communication

---

## Key Outcomes
- Eliminates manual weekly reporting
- Ensures no important updates are missed
- Improves leadership visibility with structured summaries
- Reduces effort through event-based and scheduled automation
