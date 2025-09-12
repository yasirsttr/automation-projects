# AI Chatbot for Grocery Store — n8n + Slack + Gmail

**Tools Used:** n8n · Slack (Incoming Webhook) · Gmail · Google Sheets · AI Agent (LLM) · Webhooks · JSON

## Problem
Customer support and order intake were handled manually, causing slow responses and missed orders.

## Solution
- Orchestrated an **n8n workflow** that:
  - Receives customer messages via **webhook** from an AI agent/chat widget.
  - Classifies intent (inquiry vs. order) using an **LLM**.
  - Collects/validates order details (items, quantities, address, phone).
  - Sends **order confirmation via Gmail** to the customer.
  - Notifies the team in **Slack** with order snapshot + link.
  - Logs everything to **Google Sheets** for tracking/ops.

## Flow (high level)
Webhook → Parse/Validate → LLM (classify/complete fields) → IF (order?)  
→ Gmail: confirmation to customer → Slack: notify team → Google Sheets: append row  
→ Error Handling & Dedup → Respond

## Impact
- **Faster responses** and **zero missed orders** during busy hours.  
- Centralized logging in Sheets; easier handoffs for fulfillment.  
- ~**10+ hours/week** saved vs. manual triage.

## Demo
_Add screenshots here once uploaded:_  
![Chatbot Flow](./chatbot-flow.png)  
![Sheet Log](./sheet-log.png)

## Import / Run
1. **n8n → Import from file** (`Workflow.json`) and open workflow.
2. Create credentials:
   - **Slack**: Incoming Webhook URL
   - **Gmail**: OAuth or App Password
   - **Google Sheets**: Service account / OAuth
   - **LLM**: API key (e.g., OpenAI/OpenRouter)
3. Set environment variables or node creds (see `.env.example`).
4. Activate workflow and test via webhook.

## Environment Template
Create `.env.example` in this folder:
