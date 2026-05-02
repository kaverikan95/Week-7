# AI Sensitive Data Scanner

## Overview
The AI Sensitive Data Scanner is a Python-based security and compliance tool designed to automatically identify sensitive information stored in files and source code. It combines traditional pattern matching with artificial intelligence to help organizations detect potential security risks, prioritize remediation efforts, and improve data governance.

The application scans folders recursively, identifies sensitive data such as passwords, API keys, email addresses, credit card numbers, and Social Security numbers, then uses Natural Language Processing (NLP) to assign a contextual risk level. Finally, it generates a professional Excel report for analysis and auditing.

---

## Features
- Recursive scanning of folders and subfolders
- Detection of sensitive information using Regular Expressions (Regex)
- AI-powered risk assessment using sentiment analysis
- Support for multiple file formats
- Automated Excel report generation
- Professional report formatting with headers and auto-sized columns
- Risk categorization (High, Medium, Low)

---

## Sensitive Data Types Detected
- Email Addresses
- Credit Card Numbers
- Social Security Numbers (SSN)
- API Keys
- Passwords
- Authentication Tokens
- Secrets and Credentials

---

## Supported File Types
- `.txt`
- `.csv`
- `.log`
- `.json`
- `.xml`
- `.yaml`
- `.yml`
- `.ini`
- `.config`
- `.py`
- `.js`
- `.java`
- `.env`

---

## Technologies Used
- Python 3.x
- TextBlob (Natural Language Processing)
- OpenPyXL (Excel report generation)
- Regular Expressions (Regex)
- OS module for file system traversal

---

## Installation
Install the required Python packages:

```bash
pip install textblob openpyxl
```

Download TextBlob language corpora (first-time setup only):

```bash
python -m textblob.download_corpora
```

---

## Project Structure
```text
AI-Sensitive-Data-Scanner/
│
├── sensitive_data_scanner.py
├── README.md
└── Sensitive_Data_AI_Report.xlsx
```

---

## How It Works
1. Specify the folder to scan in the `SCAN_FOLDER` configuration.
2. The application recursively scans all supported files.
3. Each line is analyzed for sensitive data patterns.
4. Matches are classified by type.
5. AI sentiment analysis evaluates contextual risk.
6. Results are exported to a formatted Excel report.

---

## Usage
Update the folder path in the script:

```python
SCAN_FOLDER = r"C:\AI-Training\ai-programmers"
```

Run the application:

```bash
python sensitive_data_scanner.py
```

---

## Output
The application generates an Excel report named:

```text
Sensitive_Data_AI_Report.xlsx
```

The report includes:
- File Name
- File Path
- Line Number
- Data Type
- Matched Text
- Risk Level

---

## AI Component
This project uses Artificial Intelligence through Natural Language Processing (NLP).

### AI Technique Used
- Sentiment Analysis via TextBlob

### Purpose
- Evaluates the contextual tone of detected sensitive data
- Assigns a risk level:
  - Negative sentiment → High Risk
  - Neutral sentiment → Medium Risk
  - Positive sentiment → Low Risk

---

## Example Console Output
```text
AI Sensitive Data Scanner
Scanning files...

Scan complete. Report saved to: C:\AI-Training\ai-programmers\Sensitive_Data_AI_Report.xlsx
Total findings: 27
```

---

## Business Benefits
- Improves data security posture
- Detects exposed credentials proactively
- Supports compliance and auditing
- Reduces manual review time
- Prioritizes remediation based on risk

---

## Future Enhancements
- Machine learning-based risk prediction
- Real-time file monitoring
- Email alert notifications
- PDF and HTML report generation
- Integration with SIEM platforms
- Cloud storage scanning (AWS S3, Azure Blob, Google Cloud Storage)
- Interactive dashboard visualization

---

## Limitations
- Sentiment analysis may not always accurately reflect security risk.
- Binary and encrypted files are not scanned.
- Regex patterns may require updates for new credential formats.

---

## License
This project is intended for educational, research, and internal security auditing purposes.

---

## Author
Developed as an AI-powered cybersecurity and data governance project using Python.

