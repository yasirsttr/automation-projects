# AI Strategy Blueprint Automation — Jotform + Zapier + AI Agent

**Tools Used:** Zapier · Jotform · Google Docs · Gmail · AI Agent (LLM)

## Problem
The client needed a way to generate **personalized strategy blueprints** for users submitting a form. Manual report writing took hours and delayed delivery.

## Solution
- Built a **Zapier workflow** to fully automate report creation:
  - **Jotform** → captures client responses and sends them into Zapier.
  - **AI Agent** → processes inputs, generates strategy text content.
  - **Google Docs** → inserts generated text into a pre-formatted template.
  - **Gmail** → automatically sends the completed PDF to the client.

## Impact
- **100% automation** of a previously manual, error-prone process.
- Delivery time reduced from **hours to minutes**.
- Professional, consistent, and scalable report generation.
- Freed team capacity to focus on higher-value client engagement.

## Flow (high level)
Jotform → Zapier Trigger → AI Agent (content generation) → Google Docs (template fill) → Gmail (send PDF)

## Demo
![Zapier Flow](./Final%20ZAP.png)  
![Jotform](./Jotform%20Form.png)

## Import / Run
1. Import Zapier workflow from `.zapier.json` or replicate steps in Zapier UI.
2. Configure integrations:
   - Jotform API key
   - Google Docs template
   - Gmail account
   - AI Agent API key
3. Test with sample form data.

