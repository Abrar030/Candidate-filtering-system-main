# 🚀 Candidate Filtering System - Human Resources Department

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)

---

## 📚 Overview
The **Candidate Filtering System** is a multi-agent, AI-powered application designed for the **Human Resources (HR) Department**.  
It automates the process of analyzing resumes, comparing them against job descriptions, and selecting the top candidates — powered by advanced NLP techniques and LLMs.

---

## ✨ Features
- **Resume Parsing and Analysis:**  
  Extract structured information from resumes in JSON format.
- **Job Description Classification:**  
  Understand and extract key requirements from job descriptions.
- **Candidate Scoring:**  
  Match and score resumes based on role, skills, experience, and education.
- **Top Candidate Selection:**  
  Automatically shortlist the top 5 candidates.
- **Interview Scheduling:**  
  Assign interview timings to the selected candidates.
- **Email Drafting:**  
  Generate personalized emails for interview invitations.

---

## 🛠️ Tech Stack
- **Python 3.8+** — Core programming language
- **LangGraph** — Managing workflows and agent state transitions
- **Streamlit** — Building the web app
- **GROQ API / LLMs** — Resume, JD analysis and grading
- **Pandas** — Data manipulation and tabular output
- **Helicone** — API monitoring and logging
- **dotenv** — Manage environment variables securely

---

## 🔁 Workflows

The system has two main pipelines:

### 1️⃣ Resume Analysis Workflow
- **Input:** Resumes (PDF) + Job Description (PDF)
- **Steps:**
  - Extract content from resumes
  - Analyze and score candidates
- **Output:** DataFrame with candidate details and scores

### 2️⃣ Email and Scheduling Workflow
- **Input:** Top 5 candidates
- **Steps:**
  - Assign interview timings
  - Generate personalized emails
- **Output:** Interview schedules and email drafts

---

## ⚙️ Installation

1. **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/Candidate-filtering-system.git
    cd Candidate-filtering-system
    ```

2. **Create a virtual environment:**
    ```bash
    python3 -m venv venv
    source venv/bin/activate   # On Windows: venv\Scripts\activate
    ```

3. **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4. **Set up environment variables:**  
Create a `.env` file inside the root folder:
    ```
    GROQ_API_KEY=your_groq_api_key
    HELICONE_API_KEY=your_helicone_api_key
    ```

---

## 🚀 Usage

1. **Launch the Streamlit app:**
    ```bash
    streamlit run app.py
    ```

2. **Inside the app:**
   - Upload resumes (PDF format) and a job description (PDF format).
   - Enter candidate interview timings.
   - Submit to view:
     - Shortlisted candidates
     - Their scores
     - Interview schedules
     - Personalized email drafts

---

## 🗂️ Project Structure

```bash
Candidate-filtering-system-main/
├── app.py                  # Main application file (Streamlit app)
├── emails.py                # Email drafting logic
├── grading_prompt.py        # Resume scoring (grading) logic
├── jd_prompt.py             # Job description classification logic
├── resume_prompt.py         # Resume parsing logic
├── timings.py               # Interview scheduling logic
├── requirements.txt         # Python dependencies
├── readme.md                # Project documentation
├── results/                 # Output files (shortlisted candidates)
├── resumes/                 # Input resumes (PDFs)
├── jd/                      # Input job descriptions (PDFs)
