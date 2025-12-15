# IT-Support-Copilot-Agent

# IT Support Copilot Agent

## Project Overview
The **IT Support Copilot Agent** is a Tier-1 IT support automation tool built using **Microsoft Copilot Studio**.  
It helps users troubleshoot common hardware, software, email, and network issues, retrieve knowledge from SOPs, classify tickets, and escalate unresolved problems to IT Support.  

This project demonstrates skills in **IT support workflows, automation, prompt engineering, and knowledge integration**.

---

## Features

- **Troubleshooting Workflows**:
  - Network / Internet connectivity
  - Slow computer
  - Email / Outlook issues
  - Account access problems

- **Knowledge Retrieval**:
  - Pulls SOP content from SharePoint / OneDrive
  - Answers common IT questions

- **Ticket Classification & Escalation**:
  - Categorizes issues (Software, Hardware, Network, Access)
  - Assigns priority and recommended team
  - Generates structured summary and optional JSON output

- **Escalation Handling**:
  - Collects additional user details
  - Prepares escalation ticket for IT Support

---

## Setup Instructions

1. Open **Microsoft Copilot Studio** and load the `IT Support Copilot Agent`.
2. Connect the **SharePoint / OneDrive Knowledge Folder** as a data source.
3. Ensure agent permissions are set so it can read SOP files.
4. Suggested prompts for testing:
   - "My internet is not working"
   - "My computer is running slow"
   - "I cannot send or receive emails on Outlook"
   - "I can’t log into my account"

---

## Usage Example

**User:** My internet is not working.  
**Bot:** Thanks for letting me know. Let’s start by checking your connection type…  

**User:** Wi-Fi  
**Bot:** Great, please check if Wi-Fi is turned on, connected to the correct network, and try restarting your Wi-Fi.  

**User:** It still doesn’t work.  
**Bot:** Collecting details for escalation…  

**JSON Escalation Output:**
```json
{
  "issue_category": "Network",
  "priority": "Medium",
  "urgency": "Normal",
  "recommended_team": "Network Team",
  "short_summary": "User in office reports no internet connectivity over Wi-Fi on a laptop. Basic troubleshooting did not resolve the issue."
}
