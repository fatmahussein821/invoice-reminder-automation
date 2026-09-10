# Invoice Reminder Automation

A scheduled **n8n invoice follow-up workflow** that reads invoice records from Airtable, calculates due-date status, identifies unpaid invoices approaching or past their due date, and sends reminder emails through Gmail.

## What it does

- Runs on a recurring schedule.
- Searches invoice records in Airtable.
- Calculates the number of days until or since the due date using Luxon/DateTime.
- Produces human-readable Arabic due-date messages such as “today” or “overdue by X days”.
- Filters for unpaid invoices with fewer than five days remaining.
- Sends a concise payment reminder through Gmail.

## Workflow architecture

`Schedule Trigger → Search Airtable records → Calculate due status → Condition → Gmail reminder`

## Integrations

- n8n
- Airtable
- Gmail
- JavaScript and Luxon date calculations

