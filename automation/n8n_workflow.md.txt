# n8n Automation Workflow

## Overview
This workflow orchestrates two automation paths:
1. Weekly Highlights (scheduled)
2. Instant MoM generation (event-driven)

## Workflow Components
- Webhook trigger (from Lovable form)
- Data validation and tagging
- Google Sheets integration
- LLM-based summarisation
- Email dispatch

## Weekly Highlights Flow
- Data captured daily and stored in Google Sheets
- Every Monday, a scheduled trigger:
  - Fetches last week's entries
  - Compiles a summary
  - Sends a consolidated email to stakeholders

## MoM Flow
- Triggered immediately on form submission
- Generates structured MoMs
- Sends email instantly

## Notes
Actual n8n JSON is excluded for simplicity and security.
