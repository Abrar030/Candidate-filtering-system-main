# 🚀 Candidate Filtering System - (GEN AI)

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)

---

## 📚 Overview
The **Candidate Filtering System** is a multi-agent, AI-powered application built for the **Human Resources (HR) Department**.  
It automates resume analysis, matches candidates against job descriptions, and identifies the best fits — all with cutting-edge NLP models.

---

## ✨ Features
- **Resume Parsing and Analysis:**  
  Extracts and structures information from resumes into JSON format.
- **Job Description Classification:**  
  Analyzes job descriptions to identify required roles, skills, qualifications, and experience.
- **Candidate Scoring:**  
  Matches resumes to job descriptions and assigns fitment scores.
- **Top Candidate Selection:**  
  Ranks and filters the top 5 candidates.
- **Interview Scheduling:**  
  Automatically assigns interview slots to shortlisted candidates.
- **Email Drafting:**  
  Generates personalized interview invitation emails.

---

## 🔁 Workflow

The system uses **LangGraph** to manage workflows and state transitions, divided into two main pipelines:

### 1️⃣ Resume Analysis Workflow
- **Input:** Resumes (PDFs) + Job Description (PDF).
- **Process:**
  - Extracts content from resumes.
  - Analyzes and scores candidates against the job description.
- **Output:**  
  A structured DataFrame containing candidate details, scores, and analysis.

### 2️⃣ Email and Scheduling Workflow
- **Input:** Top 5 shortlisted candidates.
- **Process:**
  - Assign interview timings.
  - Generate personalized email drafts.
- **Output:**  
  A DataFrame containing interview schedules and emails.

---

## ⚙️ Installation

1. **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/Candidate-filtering-system.git
    cd Candidate-filtering-system
    ```

2. **Create a virtual environment and install dependencies:**
    ```bash
    python3 -m venv venv
    source venv/bin/activate   # On Windows: venv\Scripts\activate
    pip install -r requirements.txt
    ```

3. **Set up environment variables:**  
Create a `.env` file and add the following:
    ```
    GROQ_API_KEY=your_groq_api_key
    HELICONE_API_KEY=your_helicone_api_key
    ```

---

## 🧩 Project Structure

```bash
Candidate-filtering-system-main/
├── app.py                  # Main application file (Streamlit app)
├── emails.py                #
