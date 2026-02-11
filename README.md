# Monthly-Spending-Dashboard-n8n-Google-Sheets

📌 About The Project
This project automates personal financial organization using n8n to orchestrate a complete bank statement processing workflow. The pipeline receives CSV/PDF files, processes the data, structures it in Google Sheets, and organizes files by month in Google Drive.

✅ Fully automated • ✅ Structured data • ✅ Real-time financial control


⚙️ How It Works
The n8n workflow executes the following steps:


1️⃣ Automatic Upload
Bank statements (CSV/PDF) are sent to a specific folder in Google Drive

n8n monitors the folder and triggers the workflow automatically


2️⃣ Data Processing
File is downloaded

Data extraction and cleaning

Column mapping (date, description, amount)

Information standardization


3️⃣ Structured Output
Processed data is automatically appended to a Google Sheets spreadsheet

Each transaction occupies one row with organized columns


4️⃣ Real-Time Control
The spreadsheet uses formulas to automatically calculate:

Total monthly spending

Available balance for discretionary expenses

Projections and dynamic adjustments as new expenses are recorded


🧰 Tech Stack
n8n – Workflow automation and orchestration

Google Drive API – File storage and organization

Google Sheets API – Data structuring and insertion

CSV/PDF Parsing – Bank statement extraction and standardization


🚀 How to Reproduce - Prerequisites:

n8n account

Google account with Drive and Sheets access

Bank statements in CSV or PDF format

Step-by-Step
Create a folder in Google Drive to receive the statements

Create a Google Sheets spreadsheet with the following columns:

Date

Description

Amount

In n8n, configure the following nodes:

Google Drive Trigger – monitors the folder

Google Drive – downloads the file

Extract from File – processes CSV/PDF

Edit Fields – maps and standardizes columns

Google Sheets – appends data to the spreadsheet

Set up formulas in the spreadsheet for automatic calculations

📂 Folder Structure

text

📁 Google Drive

└── 📁 Statements 

    ├── 📁 2026-01
    
    │   ├── bank_statement_2026-01-10.csv
    
    │   └── bank_statement_2026-01-25.pdf
    
    ├── 📁 2026-02
    
    └── 📁 2026-03
    
📊 Google Sheets Output Example

Date	Description	Amount

2026-01-10	Supermarket	152.30

2026-01-12	Internet Bill	89.90

2026-01-15	Restaurant	45.00

2026-01-20	Gas Station	210.75

Formulas used:

=SUMIF() – Total monthly spending

=BUDGET - TOTAL_SPENT – Available balance

=AVERAGE() – Daily spending projection

📈 Benefits
⏱️ Saves time – No manual data entry

🔍 Eliminates errors – Standardized processing

📱 Always updated – Real-time financial view

🗂️ Organized – Automatic file archiving by month
