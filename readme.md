# Job Description Skills Parser

This is a Python-based application built with Streamlit to extract and display skills from job descriptions. The app supports extracting skills using both predefined regex patterns and the Google Gemini API for advanced NLP capabilities. Users can upload job description files in `.docx` (Word) or `.pdf` formats, and the app will return a list of skills found in the text. The results can be downloaded in both Word and PDF formats.

## Features

- **Skill Extraction**: Extracts skills from job descriptions using a combination of predefined regex patterns and the Gemini API.
- **Multi-format Support**: Supports `.docx` and `.pdf` file uploads.
- **Downloadable Output**: The extracted skills can be downloaded as Word or PDF files.
- **Real-time Results**: View the extracted skills instantly in the browser.

## Requirements

Before running the application, you need to set up the following environment:

### Python Packages
You need to install the following Python packages:

- `streamlit`
- `python-docx`
- `fpdf`
- `PyPDF2`
- `google-generativeai`
- `python-dotenv`

You can install these dependencies using pip:

```bash
pip install streamlit python-docx fpdf PyPDF2 google-generativeai python-dotenv
```

### Environment Variables
Make sure you have a .env file in the root directory of your project that contains your API key for the Gemini API. The .env file should look like this:
```bash GEMINI_API_KEY=your_gemini_api_key_here ```
Replace your_gemini_api_key_here with your actual API key from Google Gemini.

### File Types Supported
- Word (.docx): Microsoft Word documents.
- PDF (.pdf): Portable Document Format files

Code Structure
```app.py```
- Main script for running the Streamlit app.
- Handles file uploads, skill extraction, and generates downloadable Word and PDF files.

Functions for skill extraction via regex and Gemini API.
```bash .env```
- Store sensitive data like API keys (e.g., for Google Gemini).

### How It Works
File Upload: Users upload a .docx or .pdf file containing a job description.
Text Extraction: The app extracts text from the uploaded file.
Skill Extraction:
Regex-based: It uses predefined skills (e.g., Python, Java, SQL, AWS) and matches them against the text.
Gemini API: It sends the text to the Gemini API to extract additional skills using advanced NLP models.
Result Generation: The extracted skills are displayed and can be downloaded as .docx or .pdf files.


Limitations
Accuracy: The accuracy of skill extraction depends on the quality of the input job description and the regex patterns.
File Complexity: Very complex or poorly formatted files might not be parsed correctly.
API Limitations: The Gemini API may have rate limits or errors depending on your API key usage.

License
This project is licensed under a proprietary license. All rights reserved. Unauthorized copying or distribution of this software, in whole or in part, is prohibited without express permission.

For licensing inquiries, please contact kavin.nr@mazosol.com . 
