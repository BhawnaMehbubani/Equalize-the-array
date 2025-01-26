# Invoice Info Extractor using Gemini

An intelligent tool for extracting key information from invoices using the Gemini platform. This project enables automated extraction, analysis, and structuring of invoice data, improving efficiency and accuracy in financial workflows.



## Table of Contents

1. [Overview](#overview)  
2. [Features](#features)  
3. [Technologies Used](#technologies-used)  
4. [Project Architecture](#project-architecture)  
5. [Setup and Installation](#setup-and-installation)  
6. [Usage](#usage)  
7. [Contributing](#contributing)  




## Overview

The **Invoice Info Extractor using Gemini** simplifies the process of managing invoices by automating the extraction of key details such as invoice numbers, dates, totals, and line items. This tool integrates with Gemini's intelligent document processing capabilities to achieve high accuracy and scalability.



## Features

- **Automated Invoice Data Extraction**: Extracts invoice numbers, dates, totals, line items, and more with minimal manual intervention.  
- **High Accuracy**: Leverages Gemini's cutting-edge AI models for precise data extraction.  
- **Multi-format Support**: Handles invoices in PDF, image, and text formats.  
- **Structured Output**: Delivers results in structured formats such as JSON or CSV for easy integration with other systems.  
- **Scalability**: Supports batch processing of multiple invoices.  



## Technologies Used

- **Python**: Backend development and data processing logic.  
- **Flask**: Lightweight framework for the web interface and API.  
- **Gemini Platform**: Intelligent document processing for invoice data extraction.  
- **PyPDF2 / PDFplumber**: PDF parsing and text extraction.  
- **Pandas**: Data manipulation and structuring.  
- **HTML/CSS/JavaScript**: User interface design and interaction.  



## Project Architecture

Below is the architecture of the **Invoice Info Extractor using Gemini** project:

```plaintext
Client (Browser)
  |
  |---> Frontend (HTML, CSS, JavaScript)
        |
        |---> File Upload Module
        |       |---> Allows users to upload invoices in PDF, image, or text formats
        |       |---> Supports multiple files for batch processing
        |
        |---> Results Display Module
                |---> Presents extracted data in a user-friendly table format
                |---> Provides options to download the structured output (JSON/CSV)
  |
  |---> Backend (Flask API)
        |
        |---> API Endpoint: /upload
        |       |---> Receives uploaded invoices
        |       |---> Validates file format and size
        |
        |---> Data Extraction Pipeline
                |
                |---> Document Parsing
                |       |---> Uses PyPDF2 and PDFplumber to extract raw text
                |       |---> Handles OCR for image-based invoices (Gemini integration)
                |
                |---> Gemini Platform Integration
                |       |---> Sends raw text data to the Gemini API
                |       |---> Receives extracted fields (e.g., invoice number, date, total, line items)
                |
                |---> Data Cleaning and Validation
                |       |---> Standardizes extracted data formats (e.g., dates, amounts)
                |       |---> Validates critical fields (e.g., checks if invoice number is valid)
                |
                |---> Post-processing
                        |---> Organizes extracted data into a structured format
                        |---> Prepares JSON and CSV outputs
  |
  |---> Storage
        |
        |---> Uploaded Invoices
        |       |---> Temporarily stores user-uploaded files
        |
        |---> Extracted Data
                |---> Stores processed data in JSON/CSV formats
                |---> Retains data temporarily for download purposes
  |
  |---> Results Delivery
        |
        |---> JSON/CSV Output
                |---> Provides downloadable structured data files
        |
        |---> API Response
                |---> Returns extracted data as a JSON response for API integration

```



## Setup and Installation

### Prerequisites

Ensure the following tools are installed on your system:  
- Python 3.8 or later  
- pip (Python package manager)  

### Installation Steps

1. Clone the repository:  
   ```bash
   git clone https://github.com/BhawnaMehbubani/Invoice-Info-Extractor-using-Gemini.git
   cd Invoice-Info-Extractor-using-Gemini
   ```

2. Create a virtual environment and activate it:  
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows, use `env\Scripts\activate`
   ```

3. Install project dependencies:  
   ```bash
   pip install -r requirements.txt
   ```

4. Set up environment variables for Gemini API credentials:  
   ```bash
   export GEMINI_API_KEY='your_api_key_here'
   export GEMINI_API_ENDPOINT='your_endpoint_here'
   ```

5. Start the application:  
   ```bash
   python app.py
   ```

6. Access the application in your browser at:  
   ```
   http://127.0.0.1:5000
   ```



## Usage

1. **Upload an Invoice**: Use the web interface to upload an invoice in PDF, image, or text format.  
2. **Extract Information**: The tool extracts key data points such as invoice number, date, total, and line items.  
3. **Download Results**: View or download the structured output in JSON or CSV format.  



## Contributing

Contributions are welcome to enhance the tool! Here's how you can contribute:  
1. Fork the repository.  
2. Create a new branch for your feature:  
   ```bash
   git checkout -b feature-name
   ```  
3. Commit your changes:  
   ```bash
   git commit -m "Add new feature"
   ```  
4. Push the changes to your fork:  
   ```bash
   git push origin feature-name
   ```  
5. Open a pull request and describe your changes.  

