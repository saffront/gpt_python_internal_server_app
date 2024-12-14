# Internal AI Web App

An internal web application that provides a chat interface to interact with GPT-4 models, with support for file uploads and analysis.

## Features

- Dual model support (GPT-4o Mini and GPT-4o)
- File upload and analysis
- Markdown rendering for responses
- File type support: PDF, Word (doc/docx), Excel (xls/xlsx), CSV, JSON, TXT
- Download responses as text files
- Conversation history management
- Responsive design

## Prerequisites

- Python 3.8+
- pip (Python package manager)
- Virtual environment (recommended)

## Installation

1. Clone the repository:
   Create and activate a virtual environment:
   python -m venv venv
   source venv/bin/activate # On Windows use: venv\Scripts\activate

Install required packages:
pip install flask python-dotenv openai PyPDF2 pandas openpyxl python-docx xlrd
Create a .env file in the project root:
touch .env # On Windows use: type nul > .env
Add your OpenAI API key to the .env file:
OPENAI_API_KEY=your_api_key_here
Project Structure
internal-ai-app/
├── app.py # Main Flask application
├── templates/ # HTML templates
│ └── index.html # Main chat interface
├── uploads/ # Temporary file upload directory
├── .env # Environment variables
├── .gitignore # Git ignore file
└── README.md # Documentation

Running the Application
Ensure your virtual environment is activated:
source venv/bin/activate # On Windows use: venv\Scripts\activate
Start the Flask application:
python app.py
Access the application at http://localhost:8080

Usage
Chat Interface
Select model type (GPT-4o Mini or GPT-4o)
Type messages in the input field
Press Enter or click Send to submit
Each model maintains its own conversation context
Switch between models using the buttons at the top
File Upload
Click the upload icon (bottom left)
Drag and drop files or click to select
Add optional message with file
Click Send to process
ESC key closes the upload dialog
Additional Features
Clear conversation: Starts a new chat
Clear History: Removes all chat history
Download: Save AI responses as text files
Markdown formatting in responses
Responsive design for mobile use
Supported File Types
PDF (.pdf)
Microsoft Word (.doc, .docx)
Microsoft Excel (.xls, xlsx)
Text files (.txt)
CSV files (.csv)
JSON files (.json)
