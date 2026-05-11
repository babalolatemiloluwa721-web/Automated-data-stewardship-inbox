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

![Workflow Canvas](Workflow%20Canvas)

---

## Request Form

The Google Form collects the following information:

- Requester Name
- Requester Email
- Dataset / Table Involved
- Data Owner
- Type of Request (Access Request / Data Definition / Data Quality Issue / Other)
- Description of Request

![Google Form](Google%20form)

---

## Google Sheets Log

All submissions are automatically logged in Google Sheets, creating a built-in audit trail of every request received.

![Google Sheet](Google%20sheet)

---

## AI-Generated Response

GPT-4 receives the full request context and generates a response that:

- Acknowledges the request professionally
- Tailors the response based on the request type
- Communicates next steps clearly
- Sets a 2-3 business day response timeline
- Maintains a professional but friendly tone

![Gmail Sent Output](Gmail%20sent%20output)

![Gmail Sent Output Again](Gmail%20sent%20output%20again)

---

## Tech Stack

- **Google Forms** - request intake
- **Google Sheets** - stores responses, triggers workflow
- **n8n** - workflow automation connecting all tools
- **OpenAI GPT-4** - drafts intelligent response emails
- **Gmail** - sends automated response to requester

---

## What This Demonstrates

- Workflow automation - connecting multiple tools without writing code
- Policy enforcement logic - AI applies governance rules to each request type
- Data stewardship in practice - automating a real daily governance task
- AI integration - using LLMs to generate policy-compliant communications
- Audit trail - all requests logged automatically in Google Sheets

---

## About

**Babalola Temiloluwa**

MS Management Information Systems - Texas Southern University (Dec 2026)

Data Governance | Workflow Automation | AI Integration | Microsoft Purview | HIPAA Compliance

babalolatemiloluwa721@gmail.com

github.com/babalolatemilouwa721-web/data-governance-portfolio
