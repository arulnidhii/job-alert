# Automated Job Alert Bot

## Description
This project is an automated job alert system that scrapes multiple job boards daily for specific keywords, filters the results, and sends a consolidated email with matching job listings. It's designed to streamline the job search process by automatically gathering relevant job postings based on user-defined criteria.

## Features
- Web scraping of multiple job boards (LinkedIn, Glassdoor, Indeed, TotalJobs)
- Keyword-based job filtering
- Daily automated execution via Windows Task Scheduler
- Personalized email alerts with matching job listings

## Technologies Used
- Python 3.x
- BeautifulSoup4 for web scraping
- Requests library for HTTP requests
- smtplib for sending emails
- Windows Task Scheduler for automation

## Installation

1. Clone this repository:

2. Navigate to the project directory:

3. Install required packages:

## Configuration

1. Open `job_alert_bot.py` in a text editor.

2. Modify the `job_boards` dictionary to include the job boards you want to scrape:
```python
job_boards = {
    'LinkedIn': 'https://www.linkedin.com/jobs/search/?keywords=your_keywords',
    'Glassdoor': 'https://www.glassdoor.com/Job/your-keywords-jobs-SRCH_KO0,17.htm',
    # Add more job boards as needed
}

```
Update the `keywords` list with your desired job search keyword
```python
keywords = ['Azure', 'databricks', 'power bi', 'SQL server']
```
Set up environment variables for email credentials:

## Open Command Prompt as administrator
Run these commands:

setx SENDER_EMAIL "your_email@gmail.com"
setx SENDER_PASSWORD "your_email_password"

## Automating with Windows Task Scheduler

1. Open Task Scheduler
2. Create a new task
3. Set it to run daily at your preferred time
4. Action: Start a program
5. Program/script: Path to your Python executable (e.g., C:\Python39\python.exe)
6. Add arguments: Path to your script (e.g., C:\Path\To\Your\job_alert_bot.py)

# Customization

1. Modify the scrape_job_board function to adjust scraping logic for different job boards.
2. Update the email template in the send_email function to change the format of the alert emails.

Contributions to improve the bot are welcome.
