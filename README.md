Resume–JD Matcher

A web-based application that compares a user’s resume with a job description using NLP, computes a match score, identifies missing skills/keywords, and suggests improvements. The tool also provides ATS-friendliness feedback to help users optimize their resumes for automated screening systems.

---

## Tech Stack

- Backend:Python, FastAPI
- NLP:spaCy, scikit-learn
- File Parsing: pdfminer.six, python-docx
- Frontend Jinja2, HTML/CSS
- Testing: pytest
- Deployment:Docker
- Version Control:Git, GitHub

---

## Features

- Upload and parse resumes (PDF/DOCX)
- Paste or upload job descriptions
- NLP-based keyword and skill extraction
- TF-IDF vectorization and cosine similarity scoring
- Missing skill/keyword identification
- Actionable rewrite suggestions for resume improvement
- ATS-friendliness feedback

---

## User Stories

- As a job seeker, I want to upload my resume and a job description so that I can see how well my resume matches the job.
- As a user, I want to see which skills or keywords are missing from my resume so I can improve it.
- As a user, I want clear suggestions on how to rewrite my resume for better alignment with the job description.
- As a user, I want feedback on whether my resume is ATS-friendly.

---

Acceptance Criteria

- The system accepts PDF and DOCX resume files.
- The system extracts and parses text from both resumes and job descriptions.
- The system displays a numeric match score after analysis.
- The system lists missing skills/keywords.
- The system provides at least one actionable rewrite suggestion for each missing skill.
- The system gives feedback on ATS-friendliness (e.g., standard section headers, formatting).

---

## Getting Started

> Note: Instructions will be updated as development progresses.

## Prerequisites

- Python 3.8+
- Git

## Setup

1. Clone the repository.

2. Create and activate a virtual environment.

3. Install dependencies.

---

## Project Structure

resume-align/
│
├── app/ # Main application code
├── tests/ # Test scripts
├── requirements.txt
├── README.md
├── .gitignore


---

## License

This project is licensed under the MIT License.

---

## Contact

For questions or collaboration, please contact [aidupogulahepsibagrace.com].

