# Automated Data Stewardship Inbox

An AI-powered workflow that automatically triages and responds to data stewardship requests built using n8n, Google Forms, OpenAI GPT-4, and Gmail.

---

## What It Does

Data stewardship teams receive requests daily, people asking for access to datasets, definitions of data fields, or reports of data quality issues. Manually responding to each one is time-consuming and inconsistent.

This project automates the entire intake and response process:

1. A requester fills out a Google Form describing their data request
2. n8n detects the new submission automatically
3. GPT-4 reads the request and drafts a professional, policy-aware response email
4. Gmail sends the response to the requester automatically no manual work needed

---

## Tech Stack

- **Google Forms** — request intake form
- **Google Sheets** — stores form responses, triggers the workflow
- **n8n** — workflow automation platform connecting all tools
- **OpenAI GPT-4** — drafts intelligent, context-aware response emails
- **Gmail** — sends the automated response to the requester

---

## Workflow Overview

```
Google Form Submission
        ↓
Google Sheets (new row added)
        ↓
n8n Trigger (detects new row)
        ↓
OpenAI GPT-4 (drafts response based on request type)
        ↓
Gmail (sends response to requester automatically)
```

---

## Request Form Fields

The Google Form collects the following information:

- Requester Name
- Requester Email
- Dataset / Table Involved
- Data Owner
- Type of Request (Access Request / Data Definition / Data Quality Issue / Other)
- Description of Request

---

## AI Prompt Logic

GPT-4 receives the full request context and generates a response that:

- Acknowledges the request professionally
- Tailors the response based on the request type (access, definition, quality issue)
- Communicates next steps clearly
- Sets expectations with a 2-3 business day response timeline
- Maintains a professional but friendly tone

---

## What This Demonstrates

- **Workflow automation** — connecting multiple tools without code
- **Policy enforcement logic** — AI applies governance rules to each request type
- **Data stewardship in practice** — automating a real daily governance task
- **AI integration** — using LLMs to generate policy-compliant communications
- **Audit trail** — all requests logged automatically in Google Sheets

---

## Screenshots

- `Workflow Canvas` — Full n8n workflow showing all nodes connected
- `gmail sent output` — Confirmed sent email output in n8n
- `Google form` — The data stewardship request intake form

---

## How to Replicate This Project

1. Create a Google Form with the fields listed above
2. Link the form to a Google Sheet
3. Create a free n8n cloud account at n8n.io
4. Add a Google Sheets trigger node — set to "On row added"
5. Add an OpenAI node — paste the prompt with dynamic field references
6. Add a Gmail node — map the To field and Message field from previous nodes
7. Publish the workflow

---

## About

**Babalola Temiloluwa**

MS Management Information Systems — Texas Southern University (Dec 2026)

Data Governance | Workflow Automation | AI Integration | Microsoft Purview | HIPAA Compliance

babalolatemiloluwa721@gmail.com

github.com/babalolatemilouwa721-web/data-governance-portfolio
