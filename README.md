# WordPress Backup Automation - n8n Workflow
An enterprise-grade n8n automation workflow that performs scheduled backups of multiple WordPress sites using All-in-One WP Migration plugin, stores them securely in Microsoft OneDrive, manages retention policies, and sends detailed email reports.

## Features
Automated Monthly Backups: Runs on the 1st of every month at 2:00 AM
Multi-Site Support: Backup multiple WordPress sites in a single workflow
All-in-One WP Migration Integration: Uses the popular WordPress backup plugin
Cloud Storage: Automatically uploads backups to Microsoft OneDrive
Retention Management: Keeps only the 5 most recent backups per site
Email Reporting: Sends detailed success/failure reports via EmailJS
Error Handling: Robust error handling with timeout protection
Clean Optimization: Excludes spam comments and post revisions from backups

🏗️ Workflow Architecture
Core Components

Monthly Backup Schedule - Cron-based trigger (1st of month, 2:00 AM)
Initialize Sites & Config - Configures sites and backup settings
Process Sites Individually - Processes each site sequentially
Trigger All-in-One Backup - Initiates WordPress backup via plugin API
Wait & Get Download Link - Polls for backup completion (up to 10 minutes)
Download Backup File - Downloads the generated .wpress file
Upload to OneDrive - Securely stores backup in Microsoft OneDrive
Get Folder Contents - Lists existing backups for retention management
Prepare Cleanup - Identifies old backups for deletion
Filter Files to Delete - Conditional logic for cleanup execution
Delete Old Files - Removes backups exceeding retention limit
Generate Report - Creates comprehensive execution summary
Send Email Report - Delivers status report via EmailJS

### Prerequisites
Required WordPress Plugin

All-in-One WP Migration plugin installed and activated on all target sites
Plugin must be accessible via WordPress admin AJAX endpoints

### Required Credentials
Microsoft OneDrive API - For cloud storage
EmailJS Account - For email notifications
WordPress Admin Access - For each site being backed up

### System Requirements
n8n version 1.0+ with JavaScript code execution enabled
Stable internet connection
Sufficient OneDrive storage space

# Usage
Automatic Execution
The workflow runs automatically on the 1st of every month at 2:00 AM via the cron schedule: 0 2 1 * *
Manual Execution

Open the workflow in n8n
Click the Execute Workflow button
Monitor progress in the execution log

### Monitoring

Execution History: Check n8n's execution history for detailed logs
Email Reports: Receive summary emails after each backup cycle
OneDrive Storage: Verify backups are stored correctly in your OneDrive

#### Email Report Format
The automated email report includes:

Execution Summary: Total sites, success/failure counts, success rate
Per-Site Status: Individual backup results for each WordPress site
Execution Details: Timestamp and completion status
Error Details: Specific error messages for failed backups
