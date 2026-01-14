# AI-Powered Sales Anomaly Monitor

Automated n8n workflow that monitors e-commerce sales data and sends intelligent alerts when week-over-week revenue drops by 10%+. Uses GPT-4 to generate human-readable incident reports from raw sales metrics.

## Features
- Email-based data ingestion (CSV attachments)
- Automated WoW percentage change calculation
- Threshold-based alerting (configurable)
- AI-generated stakeholder communications
- Multi-channel notifications (Email + Slack)
- Error handling for edge cases (insufficient data, zero baseline)
- Google Sheets logging for audit trail
- Zero-touch operation after setup

## Workflow Versions

| File | Description |
|------|-------------|
| `Monday_Morning.json` | Base template — Schedule trigger + Google Sheets input |
| `Monday_Morning_Amazon_csv.json` | Email trigger — Ingests CSV attachments from Gmail |
| `Monday_Morning_with_config.json` | Production version — Config node, Switch routing, Slack, error handling, logging |

## Tech Stack
n8n, OpenAI API (GPT-4.1-mini), Gmail API, Google Sheets API, Slack Webhooks, JavaScript

## Setup
1. Import the JSON into n8n
2. Connect your credentials (Gmail, Google Sheets, OpenAI)
3. Update the Config node with your email, Slack webhook, and threshold
4. Activate the workflow
