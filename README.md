# AI Resume Screening & Candidate Ranking System

## Project Overview
This is an intelligent resume screening application that automatically ranks and scores resumes based on a job description. It uses machine learning to match candidates with job requirements, making recruitment faster and more objective.

## What It Does
- **Upload Job Description**: Paste the job description you're hiring for
- **Upload Resumes**: Add multiple candidate resumes in PDF format
- **Automatic Ranking**: The system analyzes and scores each resume against the job description
- **Sorted Results**: View candidates ranked by match percentage (highest to lowest)

## Key Features
✓ **Fast Processing** - Quickly analyze multiple resumes  
✓ **Objective Scoring** - Uses mathematical algorithms, not human bias  
✓ **Easy to Use** - Simple web interface, no technical knowledge needed  
✓ **Multiple Resumes** - Compare and rank many candidates at once  
✓ **PDF Support** - Works with standard resume format (PDF files)  

## How It Works

### Technology Stack
- **Python** - Programming language
- **Streamlit** - Web interface framework (makes it interactive and easy to use)
- **PyPDF2** - Extracts text from PDF resume files
- **Scikit-learn** - Machine learning library for:
  - **TF-IDF Vectorization**: Converts text into numerical vectors
  - **Cosine Similarity**: Measures how similar resumes are to the job description

### Algorithm Explanation
1. **Text Extraction**: PDFs are converted to plain text
2. **Vectorization**: Both job description and resumes are converted to TF-IDF vectors (numerical representation)
3. **Similarity Calculation**: Cosine similarity compares the job description vector with each resume vector (ranges 0-1, where 1 = perfect match)
4. **Ranking**: Results are sorted with highest-matching resumes first

## How to Use

### Requirements
- Python 3.7+
- Required packages: `streamlit`, `PyPDF2`, `pandas`, `scikit-learn`

### Installation
```bash
pip install streamlit PyPDF2 pandas scikit-learn
```

### Running the Application
```bash
streamlit run resume_app.py
```

The app will open in your browser. Then:
1. Paste or enter the **Job Description** in the text box
2. Click **Upload PDF files** and select one or more resume PDFs
3. The system automatically ranks and displays results in a table

## Output
The application displays a table with:
- **Resume**: Name of the uploaded resume file
- **Score**: Similarity score (0.0 to 1.0) - higher is better match

## Use Cases
- **Recruitment Departments**: Screen hundreds of resumes quickly
- **HR Teams**: Identify top candidates automatically
- **Job Boards**: Auto-match candidates to jobs
- **Career Services**: Help students find matching opportunities

## Limitations & Future Improvements
- Currently matches on text similarity only
- Doesn't evaluate work experience depth or soft skills
- Future: Add parsing for specific skills, experience levels, certifications
- Future: Support for more file formats (DOCX, DOC, etc.)

## Project Status
This is a capstone project for AICET Internship program - demonstrating practical application of machine learning in real-world recruitment scenarios.

---

**Questions?** Feel free to reach out or check the code comments in `resume_app.py`
