# Capacity Filter Workflow – GoHighLevel (GHL) → n8n

## Problem
The client needed a way to prevent sales pipeline overload in GoHighLevel by limiting the number of active leads in a sales pipeline.

## Solution
- Created an **n8n workflow** that:
  - Receives form submissions from GHL via webhook.
  - Checks current open opportunities through LeadConnector API.
  - Tags contacts as **ACTIVE** or **WAITLIST** depending on pipeline capacity.
  - Sends back response to GHL with decision.

## Impact
- Eliminated manual lead triaging.
- Prevented pipeline bottlenecks.
- Improved team efficiency with deterministic, automated lead assignment.

## Tools Used
- n8n
- GoHighLevel (LeadConnector API)
- Webhooks
- JavaScript (capacity calculation)

## Demo
![WorkFlow_n8n](./Workflow%20execution.png)
![WorkFlow_GHL](./GHL%20Workflow.png)
![Pipeline](./Pipelpine%20stages.png)
