# JobScraper AI

AI-Powered Job Scraper with Smart Resume Optimization

## Overview

JobScraper AI is a comprehensive job tracking platform that automates job discovery from Indeed and LinkedIn, and uses Google Gemini Pro to generate ATS-optimized resumes tailored to each job description.

## Features

- **Multi-Platform Job Scraping**: Scrape jobs from Indeed and LinkedIn without APIs
- **Intelligent Job Matching**: Filter jobs based on skills, sponsorship, experience level, and more
- **AI-Powered Resume Optimization**: Generate tailored resumes using Gemini Pro with 90+ ATS score targeting
- **Batch Resume Generation**: Create optimized resumes for multiple jobs simultaneously
- **Job Tracking Dashboard**: Track applications and manage your job search

## Tech Stack

- **Backend**: Python 3.12, Flask 2.3.3
- **Scraping**: Selenium 4.12.0, Undetected ChromeDriver
- **AI**: Google Gemini Pro API
- **Database**: MySQL
- **Frontend**: HTML5, CSS3, JavaScript, Bootstrap 5.3.0

## Setup Instructions

### Prerequisites

- Python 3.12 or higher
- MySQL database
- Chrome browser (for Selenium)
- Google Gemini API key

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/jobscraper-ai.git
   cd jobscraper-ai
   ```

2. **Create virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Edit .env and add your:
   # - GEMINI_API_KEY
   # - MySQL database credentials
   ```

5. **Configure database**
   - Update `db_config.py` with your MySQL credentials
   - Create the database schema (tables will be created automatically)

6. **Run the application**
   ```bash
   python app.py
   ```

7. **Access the application**
   - Open browser: `http://localhost:5000`

## Usage

1. **Upload Resume**: Go to Profile page and upload your resume (PDF or DOCX)
2. **Scrape Jobs**: Use the Scraper page to search for jobs on Indeed or LinkedIn
3. **View Results**: Check the Results page to see scraped jobs
4. **Optimize Resumes**: Use Batch Optimize to generate tailored resumes for multiple jobs
5. **Track Applications**: Use the Tracker to manage your job applications

## Project Structure

```
jobscraper-ai/
├── app.py                      # Main Flask application
├── simple_resume_optimizer.py  # Resume optimization with Gemini
├── resume_parser.py            # Resume parsing and extraction
├── job_precheck.py             # Job filtering logic
├── db_config.py                # Database configuration
├── MASTER_RESUME_PROMPT.py     # Gemini prompt templates
├── scrapers/                   # Web scraping modules
│   ├── indeed_scraper.py
│   ├── linkedin_scraper.py
│   └── linkedin_connection.py
├── templates/                 # HTML templates
├── uploads/                   # User uploaded resumes
├── results/                   # Scraped job data
└── temp/resumes/              # Generated optimized resumes
```

## API Keys Required

- **Google Gemini API Key**: Get from [Google AI Studio](https://makersuite.google.com/app/apikey)

## License

This project is built for PatriotHacks Fall 2025 hackathon.

## Contributors

- Chandrashakar Gudipally

## Acknowledgments

- Built with Google Gemini Pro API
- Uses Selenium for web scraping
- Flask for web framework

