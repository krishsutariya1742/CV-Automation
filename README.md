# CV-Automation

## Workflow Summaries

### Workflow 1 — Daily CV Processing
- Trigger: New Outlook email received.
- Verify the email is a job application and retrieve attachments.
- Convert attachments to files and extract text.
- Fetch open positions from Airtable.
- Use Claude AI to match CVs against openings and produce: best-match title, score (0–100), skills & experience analysis, and final recommendation.
- Mark email as read; store extracted candidate details in Airtable if available.
- Shortlist candidates with AI score ≥ 80 and send an HR report by email.

![Workflow 1 diagram](/DAILY%20CV%20PROCESSING.png)

### Workflow 2 — New Job Opening Match
- Trigger: New record added to the Job Openings table in Airtable.
- Confirm the opening status is "Open" and retrieve all candidates.
- Use Claude AI to re-evaluate candidates against the new job: updated score (0–100), status, and recommendation.
- Create records for shortlisted and interviewed candidates.
- Shortlist candidates with AI score ≥ 80 and send an HR report by email.

![Workflow 2 diagram](/NEW%20JOB%20OPENING%20MATCH.png)

### Workflow 3 — Send Candidate Report
- Trigger: Every day at 9:00 AM
- Retrieve job openings from Airtable.
- For each job, fetch shortlisted candidates and rank by AI score.
- Select the top 5 candidates per job.
- Send a job-wise candidate report to HR (table format).

![Workflow 3 diagram](/Send%20Candidate%20Report.png)
