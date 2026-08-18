# ai-recruitment-automation-n8n
End-to-end AI recruitment automation platform built using n8n. Features dynamic candidate evaluation via LLMs, multi-stage HR decision webhooks, Google Calendar scheduling, automated candidate communication, and weekly metrics reporting with global error handling.
# AI-Powered Recruitment & Hiring Automation Platform (n8n)

An end-to-end multi-workflow automation engine built with n8n to streamline candidate ingestion, LLM-based screening, HR approvals, interview scheduling, and weekly pipeline reporting.

## 📌 Architecture Overview

The system consists of four interconnected sub-workflows:

1. **WF1 - Candidate Evaluation Engine:** Ingests candidate applications via Webhook, logs details in Google Sheets, evaluates resumes using Groq/OpenAI LLM APIs, and triggers conditional email pathways.
2. **WF2 - HR Approval Portal:** Generates dynamic review emails to HR with approve/reject webhook links, processing decisions to route candidates further.
3. **WF3 - Automated Interview Scheduling:** Receives slot selections, creates Google Calendar events, updates candidate tracking statuses, and dispatches calendar invites.
4. **WF4 - Analytics Generator & Error Recovery:** Runs on a weekly cron schedule to calculate recruitment metrics via JavaScript, dispatches executive summary reports, and catches pipeline errors using a Global Error Trigger to alert administrators.

---

## 🛠️ Repository Structure

```text
.
├── workflows/
│   ├── WF1_Main_Workflow.json
│   ├── WF2_HR_Approval_Portal.json
│   ├── WF3_Automated_Interview_Scheduling.json
│   └── WF4_Analytics_And_Error_Recovery.json
└── README.md
