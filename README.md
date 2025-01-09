# AI-Powered-Resume-Parser-Classifier

# AI-Powered Resume Parser & Classifier

This project is an AI-powered tool that analyzes resumes and compares them with job descriptions to determine how well they match. The system extracts key skills from both the resume and the job description, performs a similarity analysis, and provides feedback on which skills are present and which are missing. This is useful for both job seekers and recruiters to evaluate the fit of a candidate for a specific job role.

## Features
- **Skill Extraction**: Extracts and matches skills from resumes and job descriptions.
- **Similarity Scoring**: Provides a similarity score to quantify how well a resume matches a job description.
- **Matched and Missing Skills**: Returns a list of skills found in the resume and those missing based on the job description.

## Installation & Setup

### Prerequisites

Before you run the app, make sure you have **Python 3.6+** installed. You will also need the following Python packages:

1. **Flask**: Web framework to serve the application.
2. **Transformers**: Hugging Face library to leverage pre-trained models like BERT for text embeddings.
3. **spaCy**: Natural Language Processing library for text processing and tokenization.
4. **FuzzyWuzzy**: Python library for fuzzy string matching.
5. **PyPDF2**: Python library for reading and extracting text from PDF files.
6. **python-docx**: Python library for extracting text from `.docx` files.
7. **Selenium**: Web scraping tool for extracting job descriptions from websites.
8. **webdriver-manager**: To manage the WebDriver installation for Selenium.

### Install Required Libraries

First, clone the repository to your local machine:

git clone https://github.com/yourusername/resume-parser.git
cd resume-parser

Then, create a virtual environment (optional but recommended):

bash
Copiar código
Download
python -m venv venv
source venv/bin/activate  # For Linux/MacOS
venv\Scripts\activate  # For Windows
Install the required dependencies using pip:

bash
Copiar código
Download
pip install -r requirements.txt
Additional Setup for Selenium (Web Scraping)
To extract job descriptions from websites like LinkedIn or Indeed, you will need to install Chrome WebDriver.

Download ChromeDriver: You can download it manually or let webdriver-manager handle the installation. The code will automatically manage the driver using the ChromeDriverManager library.

If you encounter issues, ensure you have Google Chrome installed on your machine, and the ChromeDriver version is compatible with it.

Required Files
resume.py: Main Python script that handles the resume parsing and classification.
index.html: HTML file that serves the front-end of the application for file uploads and displaying results.
requirements.txt: A list of all the required Python libraries for the project.
How to Use the Application
Run the Flask App:

Start the Flask server by running the following command in your terminal:

bash
Copiar código
Download
python resume.py
The app will start on http://127.0.0.1:5000 by default.

Upload Resume and Job Description:

Visit the web interface (http://127.0.0.1:5000) and upload the resume file (supports PDF, DOCX, or TXT formats).
Provide the URL of a job description (from LinkedIn, Indeed, or any job board).
Optionally, specify the job role (e.g., software engineer, data scientist).
Get Results:

The app will return the following details:

Similarity Score: A number between 0 and 1 indicating how similar the resume is to the job description.
Category: The similarity category (e.g., Extremely High, High, Medium).
Matched Skills: A list of skills found in both the resume and job description.
Missing Skills: A list of skills required by the job but missing in the resume.
Example
json
Copiar código
Download
{
  "category": "Extremely High",
  "explanation": "The resume and job description are extremely similar. The candidate is a perfect match.",
  "matched_skills": ["teamwork", "excel", "project management"],
  "missing_skills": ["communication", "leadership", "critical thinking", "data analysis"],
  "similarity_score": 0.9179621934890747
}
Files in the Repository
1. resume.py:
The main script for processing resumes and job descriptions.
Extracts text from the resume, performs text normalization, and compares skills.
Handles file uploads and web scraping for job descriptions.
2. index.html:
The front-end of the application that allows users to upload files and enter job description URLs.
3. requirements.txt:
A list of all dependencies required to run the application.
Known Issues
The web scraping feature might be blocked by websites like Indeed or LinkedIn, especially when extracting job descriptions from them.
Ensure that Google Chrome is installed and up-to-date for Selenium to work properly.
Future Improvements
Add support for more file formats (e.g., .rtf, .odt).
Enhance the fuzzy matching process to be more lenient.
Integrate additional features like applying filters for required skills based on industry-specific requirements.
License
This project is licensed under the MIT License - see the LICENSE file for details.

markdown
Copiar código
Download

### Save the File:
1. Open a **text editor** like Notepad or VS Code.
2. Paste the content above.
3. Save the file as `README.md`.

Let me know if you need any further assistance!
