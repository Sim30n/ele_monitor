# README: Setting Up Crontab for ensto_e.py

## Description
This guide explains how to set up a cron job to run `ensto_e.py` daily at midnight.

## Prerequisites
- Ensure you have Python installed in the specified virtual environment.
- create .env file with ensto_e token. See .env.example file.
- Confirm that the script `<path_to_project>/web_app/ensto_e.py` is executable.
- The user running the cron job should have the necessary permissions.

## Steps to Set Up Crontab

1. Open the crontab editor:
   ```
   crontab -e
   ```

2. Add the following line at the end of the file:
   ```
   0 0 * * * <path_to_project>/web_app/venv/bin/python <path_to_project>/web_app/ensto_e.py
   ```
   This schedules the script to run at **midnight (00:00) every day**.

3. Save and exit the editor.

## Verify Crontab is Set
To check if the cron job is added, run:
```
crontab -l
```
This should display the scheduled job.

## Troubleshooting
- Check logs for errors:
  ```
  grep CRON /var/log/syslog
  ```
- Ensure the script runs manually:
  ```
  <path_to_project>/web_app/venv/bin/python <path_to_project>/web_app/ensto_e.py
  ```
- If it fails, ensure the virtual environment is correctly set up.

## Notes
- To edit or remove the cron job, use `crontab -e`.
- Changes to the script require no modifications to the crontab unless paths change.

