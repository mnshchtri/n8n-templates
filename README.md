# n8n Templates: Personal Assistant & Cybersecurity Agents

This repository contains a collection of n8n workflow templates designed to automate and enhance productivity for personal assistant and cybersecurity tasks. Each template is a ready-to-import JSON file for use with [n8n](https://n8n.io/), the extendable workflow automation tool.

## Directory Structure

```
PA/
  CalendarAgent.json
  EmailAgent.json
  PhoneCallAgent.json
  ThreatIntelAggregator.json
  AlertSuspiciousLogin.json
  PhishingReportTriage.json
  SIEM_EDR_Integration.json
  IP_DomainReputationChecker.json
  DailyVulnNewsSummary.json
```

## Personal Assistant Templates

### 1. CalendarAgent
Automates calendar management using Google Calendar. Capabilities include:
- Creating events (with or without attendees)
- Retrieving and summarizing events for specific dates
- Integrates with OpenAI for natural language understanding

**Requirements:**
- Google Calendar OAuth2 credentials
- OpenAI API credentials

### 2. EmailAgent
Manages email tasks via Gmail. Capabilities include:
- Sending emails with custom subject and body
- Retrieving emails (optionally filtered by sender or unread status)
- Uses OpenAI for natural language processing of email tasks

**Requirements:**
- Gmail OAuth2 credentials
- OpenAI API credentials

### 3. PhoneCallAgent
Automates phone call tasks using the Vapi.ai API. Capabilities include:
- Initiating phone calls to specified numbers
- Customizing call parameters (purpose, tone, instructions, etc.)
- Monitoring call status and summarizing results

**Requirements:**
- Vapi.ai API credentials

## Cybersecurity Templates

### 1. ThreatIntelAggregator
Aggregates threat intelligence from VirusTotal and AbuseIPDB. Capabilities include:
- Accepts an IP address or domain as input
- Queries both VirusTotal and AbuseIPDB for reputation and threat data
- Aggregates and outputs the results for enrichment or alerting

**Requirements:**
- VirusTotal API credentials
- AbuseIPDB API credentials

### 2. AlertSuspiciousLogin
Alerts on suspicious logins or IP addresses. Capabilities include:
- Accepts login event data (e.g., via webhook)
- Checks the login IP against AbuseIPDB
- Sends an alert email if the IP is flagged as suspicious (abuse confidence score ≥ 50)

**Requirements:**
- AbuseIPDB API credentials
- SMTP credentials for sending alert emails

### 3. PhishingReportTriage
Automates phishing report triage. Capabilities include:
- Accepts a reported email (e.g., via webhook)
- Extracts URLs/domains from the email body
- Checks each URL against VirusTotal
- Sends a triage summary email to the security team

**Requirements:**
- VirusTotal API credentials
- SMTP credentials for sending triage summary emails

### 4. SIEM_EDR_Integration
Generic integration for forwarding security events to a SIEM or EDR platform. Capabilities include:
- Accepts security event data (e.g., via webhook)
- Forwards the event to a configurable SIEM/EDR HTTP endpoint
- Optionally sends a confirmation email to the security team

**Requirements:**
- SIEM/EDR HTTP endpoint (configure in the workflow)
- SMTP credentials for sending confirmation emails (optional)

### 5. IP_DomainReputationChecker
Checks the reputation of an IP address or domain. Capabilities include:
- Accepts an IP or domain (e.g., via webhook)
- Checks the domain with VirusTotal
- Checks the IP with AbuseIPDB
- Aggregates and returns a summary of the reputation

**Requirements:**
- VirusTotal API credentials
- AbuseIPDB API credentials

### 6. DailyVulnNewsSummary
Sends a daily summary of the latest vulnerability news. Capabilities include:
- Fetches the latest vulnerability news from an RSS feed (e.g., NVD)
- Summarizes the top items
- Sends an email summary to the security team

**Requirements:**
- SMTP credentials for sending summary emails

---

## Usage Instructions

1. **Import a Template:**
   - In your n8n instance, go to 'Workflows' > 'Import from File'.
   - Select the desired JSON file from the `PA/` directory.

2. **Configure Credentials:**
   - Set up the required credentials (Google, Gmail, OpenAI, Vapi.ai, VirusTotal, AbuseIPDB, SMTP, or SIEM/EDR endpoint) in n8n's Credentials section.
   - Update any credential references in the imported workflow if needed.

3. **Customize and Run:**
   - Adjust workflow parameters as needed for your use case.
   - Activate and trigger the workflow as desired.

## Notes
- These templates are intended as starting points. You can extend or modify them to fit your specific needs.
- Ensure you do **not** commit sensitive credential information to version control.

## License
MIT 