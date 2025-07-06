# n8n Templates: Personal Assistant Agents

This repository contains a collection of n8n workflow templates designed to automate and enhance productivity for personal assistant tasks. Each template is a ready-to-import JSON file for use with [n8n](https://n8n.io/), the extendable workflow automation tool.

## Directory Structure

```
PA/
  CalendarAgent.json
  EmailAgent.json
  PhoneCallAgent.json
```

## Templates Overview

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

## Usage Instructions

1. **Import a Template:**
   - In your n8n instance, go to 'Workflows' > 'Import from File'.
   - Select the desired JSON file from the `PA/` directory.

2. **Configure Credentials:**
   - Set up the required credentials (Google, Gmail, OpenAI, or Vapi.ai) in n8n's Credentials section.
   - Update any credential references in the imported workflow if needed.

3. **Customize and Run:**
   - Adjust workflow parameters as needed for your use case.
   - Activate and trigger the workflow as desired.

## Notes
- These templates are intended as starting points. You can extend or modify them to fit your specific needs.
- Ensure you do **not** commit sensitive credential information to version control.

## License
MIT 