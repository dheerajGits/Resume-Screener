# Automated Resume Screening and Microsoft Form Submission with RPA

## Objective:
Develop a bot that automates the screening of resumes and inputs candidate details into a Microsoft Form, streamlining the recruitment process for HR teams.

## Problem Statement:
HR teams often manually review a high volume of resumes to identify qualified candidates. This repetitive and time-consuming task is prone to errors, leading to potential oversight of suitable candidates. Automating the initial screening phase can significantly reduce time spent, improve accuracy, and provide an audit trail for future reference.

## Scope:
- **Input:** Emails with the subject line “STGi | New Hire(s)” that contain a PDF form attachment.
- **Output:** Automatically extract details from the PDF form, populate a Microsoft Form, and generate an audit report of all processed forms for the day.

## Key Features:
1. **Email Fetching and Filtering:**
   - Retrieve emails from a specified inbox.
   - Filter based on the subject line “STGi | New Hire(s)”.
2. **Attachment Download:**
   - Download PDF attachments and store them in a designated folder for processing.
3. **Data Extraction:**
   - Use RPA tools and OCR to extract key details (e.g., candidate name, education, skills, years of experience) from the PDF forms.
4. **Microsoft Form Submission:**
   - Automatically populate the Microsoft Form with the extracted data.
   - Use dynamic selectors or UI Descriptors to manage form field variations during each execution.
5. **Audit Report Generation:**
   - Create a detailed audit report that logs all submissions processed each day, adhering to the provided report template.
6. **Daily Email Report:**
   - Email the generated audit report at the end of each process cycle, summarizing all items processed.
7. **Error Handling and Logging:**
   - Implement robust error handling to manage issues such as email retrieval failures or incorrect PDF formats.
   - Maintain comprehensive logs to track errors, processed items, and system performance, enabling efficient auditing and troubleshooting.

## Tools & Technologies:
- **RPA Platforms (e.g., UiPath):** 
- Microsoft Excel for data manipulation
- Email Platforms (e.g., Outlook, Gmail) for communication and report distribution

## Links:
- [Resume Screening Pre-Requisites](https://github.com/stg-india/hackathon-september-2024/tree/96f5d2a6c61335901bfe7180bb9617aaf2de9f41/ResumeScreening%20-%20PreRequisites)  
- **Microsoft Form:** [Link to Form](https://forms.office.com/r/LDWeShviUF)
