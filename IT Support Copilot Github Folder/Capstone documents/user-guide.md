# IT Support Copilot Agent — User Guide

## Overview
The **IT Support Copilot Agent** automates Tier-1 IT support tasks, assisting users with troubleshooting common hardware, software, email, and network issues.  
It retrieves knowledge from SOPs, classifies tickets, and escalates unresolved problems to IT Support.  

This guide is for both users and administrators.

---

## Getting Started

### Accessing the Agent
1. Open **Microsoft Copilot Studio**.
2. Select **IT Support Copilot Agent** from your list of agents.
3. Ensure your device has internet access to retrieve knowledge from SharePoint/OneDrive.

### Knowledge Sources
- SOPs and troubleshooting guides are stored in **SharePoint / OneDrive**.
- Ensure the agent has **read permissions** for the folder.

---

## Using the Agent

### Suggested Prompts
Start a workflow by typing any of the following:
- "My internet is not working"
- "My computer is running slow"
- "I cannot send or receive emails on Outlook"
- "I can’t log into my account"

### Example — Network Issue Workflow

**Step 1:** User input: `"My internet is not working"`  
**Step 2:** Bot asks connection type: Wi-Fi / Ethernet / Not sure  
**Step 3:** User input: `"Wi-Fi"`  
**Step 4:** Bot provides troubleshooting steps:
1. Check if Wi-Fi is turned on  
2. Confirm connection to the correct network  
3. Restart Wi-Fi  

**Step 5:** If the issue persists:
- Bot collects additional details:
  - Location (Office / Remote)  
  - Device type (Laptop / Desktop / Mobile)  
  - Error messages  
  - Business impact  

**Step 6:** Bot prepares an escalation ticket.

**Ticket JSON Example:**
```json
{
  "issue_category": "Network",
  "priority": "Medium",
  "urgency": "Normal",
  "recommended_team": "Network Team",
  "short_summary": "User in office reports no internet connectivity over Wi-Fi on a laptop. Basic troubleshooting did not resolve the issue."
}
