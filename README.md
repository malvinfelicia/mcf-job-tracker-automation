# 🤖 MCF Job Tracker Automation

An automated daily job tracking system built with n8n that fetches relevant job listings from the MyCareersFuture (Singapore) public API every morning at 9am SGT.

## 🎯 Purpose
Built to automate my personal job search — filters relevant roles matching my background (Business Analyst, Lecturer, Research Fellow, Postdoc), sends instant Telegram notifications, and logs all matches to Google Sheets for daily review.

## ⚙️ How It Works
1. **Schedule Trigger** — runs daily at 9:00 AM Singapore Time
2. **HTTP Request** — fetches jobs from MyCareersFuture public API
3. **Split Out** — splits API response into individual job items
4. **Filter (Keywords)** — keeps only relevant job titles
5. **Filter (Date)** — keeps only jobs posted in last 3 days
6. **Code in JavaScript** — extracts and cleans job fields
7. **Telegram** — sends formatted job alert message
8. **Google Sheets** — logs all matched jobs for review

## 🛠 Tech Stack
| Tool | Purpose |
|---|---|
| n8n | Workflow automation |
| MyCareersFuture API | Singapore job listings source |
| JavaScript | Data extraction and cleaning |
| Telegram Bot API | Real-time job notifications |
| Google Sheets API | Job tracking and logging |

## 📋 Job Roles Tracked
- Business Analyst
- Research Fellow
- Assistant Professor
- Lecturer
- Postdoc (with stipend)
- Teaching Associate

## 📊 Google Sheets Output
Each matched job is logged with:
- Job Title
- Company
- Salary Range
- Job Type
- Posted Date
- Required Skills
- Job Description
- Apply Link

## 🔧 Setup Instructions
1. Import `workflow.json` into your n8n instance
2. Configure your credentials:
   - Google Sheets OAuth2
   - Telegram Bot API key
3. Update the Filter node keywords to match your target roles
4. Set your Schedule Trigger timezone
5. Activate the workflow

## 👤 Author
**Malvin Felicia Ponnurajan**  
PhD Scholar | Business Analyst | Organizational Behavior Researcher  
Singapore

[![GitHub](https://img.shields.io/badge/Portfolio-malvinfelicia-blue)](https://github.com/malvinfelicia)
