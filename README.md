# 🤖 AI Job Hunt Agent — Automated Job Discovery & Application Assistant

An intelligent, AI-powered job search automation system designed to simplify and optimize the job-hunting process.

The **AI Job Hunt Agent** automatically scans **2,000+ job postings every morning at 6:00 AM**, filters relevant opportunities based on predefined preferences, evaluates job descriptions using Large Language Models (LLMs), and delivers a personalized email digest containing the **Top 5 most relevant job opportunities**.

But it doesn't stop at finding jobs — it also generates **job-specific resume bullet points and personalized cover notes**, helping candidates prepare for applications more efficiently.

The goal is to transform traditional, time-consuming job searching into an intelligent, automated, and personalized experience.

## 🚀 Key Features

### 1. Automated Job Discovery
- Scans 2,000+ job postings daily.
- Collects opportunities from multiple company career platforms.
- Integrates with Greenhouse, Lever, and Ashby public job APIs.
- Extracts essential information, including job title, company, location, description, and application URL.

### 2. Intelligent Job Filtering
- Uses configurable filters to eliminate irrelevant opportunities.
- Matches job titles against predefined inclusion and exclusion rules.
- Filters opportunities based on skills, experience, job type, and other preferences.
- Reduces thousands of raw postings to a smaller set of relevant candidates before AI processing.

### 3. AI-Powered Job Matching & Scoring
- Uses LLMs to analyze job descriptions and candidate profiles.
- Evaluates how closely each opportunity matches the candidate's skills, experience, and career interests.
- Assigns relevance scores to job opportunities.
- Ranks shortlisted jobs based on their overall suitability.

### 4. Personalized Resume Bullet Generation
- Analyzes job requirements and identifies important skills and keywords.
- Generates tailored resume bullet suggestions for individual job descriptions.
- Helps candidates highlight relevant projects, technical skills, and experience.
- Keeps suggestions grounded in the candidate's actual profile rather than inventing qualifications.

### 5. AI-Generated Cover Notes
- Creates personalized cover notes for shortlisted opportunities.
- Adapts the content to the company, role, and job requirements.
- Produces application-ready drafts that candidates can review and customize.

### 6. Automated Email Digest
- Delivers a daily email containing the Top 5 ranked job opportunities.
- Includes company names, job titles, match scores, and application links.
- Provides tailored resume suggestions and cover notes.
- Uses SMTP to automate daily email delivery.

### 7. Scheduled Automation
- Runs automatically every morning at **6:00 AM**.
- Uses GitHub Actions for scheduled execution.
- Eliminates the need to manually run the job search pipeline every day.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core automation and processing |
| Greenhouse API | Job posting collection |
| Lever API | Job posting collection |
| Ashby API | Job posting collection |
| Gemini / Groq / Claude | AI-based job matching and content generation |
| SMTP | Automated email delivery |
| GitHub Actions | Scheduled workflow execution |
| YAML | Configuration and customizable filtering |

## ⚙️ How It Works

The system follows a multi-stage automated pipeline:

**Step 1 — Job Collection**

Fetches job postings from supported public career APIs across multiple companies.

**Step 2 — Data Processing**

Cleans, normalizes, and structures raw job posting data to maintain consistency.

**Step 3 — Rule-Based Filtering**

Applies configurable filters to remove irrelevant roles and reduce unnecessary AI processing.

**Step 4 — AI Evaluation**

Uses an LLM to evaluate shortlisted jobs against the candidate's profile and calculate relevance scores.

**Step 5 — Job Ranking**

Sorts evaluated opportunities and selects the five highest-ranked matches.

**Step 6 — Personalized Content Generation**

Generates relevant resume bullet suggestions and customized cover notes for each selected job.

**Step 7 — Email Delivery**

Compiles all results into a structured email digest and sends it to the candidate.

**Step 8 — Daily Scheduling**

GitHub Actions automatically triggers the complete workflow every morning at 6:00 AM.

## 🏗️ System Architecture

```text
       GitHub Actions Scheduler
              (6:00 AM)
                  |
                  v
          Job Collection Layer
                  |
       +----------+----------+
       |          |          |
   Greenhouse   Lever      Ashby
       |          |          |
       +----------+----------+
                  |
                  v
          Data Processing
                  |
                  v
         Rule-Based Filtering
                  |
                  v
          AI Matching Engine
          (Gemini / Groq /
               Claude)
                  |
                  v
          Job Scoring & Ranking
                  |
                  v
           Top 5 Selection
                  |
           +------+------+
           |             |
           v             v
      Resume Bullets  Cover Notes
           |             |
           +------+------+
                  |
                  v
           Email Generator
                  |
                  v
             SMTP Delivery
                  |
                  v
          Daily Job Digest
```

## 🎯 Why This Project?

Finding relevant job opportunities is one of the most repetitive parts of the job application process. Candidates often spend hours browsing multiple career websites, comparing job descriptions, checking eligibility, and customizing application materials.

This project addresses that problem through automation and AI.

Instead of manually searching through thousands of listings, candidates receive a curated selection of relevant opportunities with personalized application assistance directly in their inbox.

## 💡 Key Learning Outcomes

Building this project involved practical experience with:

- Integrating multiple third-party public APIs.
- Building automated data collection pipelines.
- Designing rule-based filtering systems.
- Implementing LLM-powered evaluation and ranking.
- Writing effective prompts for structured AI outputs.
- Generating personalized content using candidate profiles.
- Automating email delivery using SMTP.
- Scheduling Python workflows using GitHub Actions.
- Managing configuration and environment variables securely.
- Optimizing AI API usage by filtering data before LLM processing.

## 🔮 Future Enhancements

- Add more job board integrations.
- Introduce historical job tracking and duplicate detection.
- Build a web dashboard to visualize job matches.
- Add application status tracking.
- Introduce feedback-based personalization to improve future rankings.
- Support multiple candidate profiles.
- Add job alerts based on newly discovered opportunities.

## 🔐 Configuration & Security

- API keys and email credentials are managed through environment variables and GitHub Secrets.
- Configurable job filters allow users to personalize their search without modifying the core Python code.
- Public job APIs are used for job discovery.
- AI provider integration is designed to support multiple LLM providers.

## 👨‍💻 Project Vision

**Build smarter. Search less. Apply better.**

The AI Job Hunt Agent demonstrates how Python automation, public APIs, and Large Language Models can work together to solve a real-world problem.

It is more than a job scraper — it is an intelligent job discovery and application preparation assistant designed to make the job search process faster, smarter, and more personalized.

---

**Built with ❤️ using Python, AI, APIs, and Automation.**
