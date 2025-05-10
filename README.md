# Government Scheme Navigator

A chatbot web application that provides information about Indian government schemes using OpenAI's GPT-3.5 Turbo and Gradio. The assistant is designed to answer user queries and guide them to suitable central and state-level government schemes.

## Features

- Built with OpenAI GPT-3.5 Turbo
- Natural language conversation
- Remembers previous questions for context
- Easy-to-use Gradio interface
- Custom system prompt focused on Indian government schemes

## Requirements

- Python 3.7 or above
- OpenAI API key (available at https://platform.openai.com/)
- The following Python packages:
  - openai
  - gradio
  - python-dotenv (optional for loading environment variables)

## Installation

1. Clone or download the repository.

2. (Optional) Create a virtual environment:

   ```bash
   python -m venv venv
   # Activate on Windows
   venv\Scripts\activate
   # Or on macOS/Linux
   source venv/bin/activate
Install dependencies:

bash
Copy
Edit
pip install openai gradio
Or, if you have a requirements.txt:

bash
Copy
Edit
pip install -r requirements.txt
Set your OpenAI API key:

Option 1: Hardcode it in the script (not recommended for production)

python
Copy
Edit
openai.api_key = "your-api-key"
Option 2: Use a .env file (recommended)

ini
Copy
Edit
OPENAI_API_KEY=your-api-key-here
Add this to your Python code:

python
Copy
Edit
from dotenv import load_dotenv
import os
load_dotenv()
openai.api_key = os.getenv("OPENAI_API_KEY")
Running the App
Run the Python script:

bash
Copy
Edit
python app.py
This will open a Gradio interface in your web browser.

How It Works
The chatbot uses OpenAI's gpt-3.5-turbo model.

A system prompt tells the assistant to act as an expert on Indian government schemes.

It stores previous messages to maintain context in the conversation.

The Gradio interface collects user input and displays AI responses.

Example Queries
What are the schemes available for girl education in Maharashtra?

Tell me about any central government schemes for startups.

Are there any subsidies for farmers in Tamil Nadu?

Security
Do not expose your OpenAI API key in public code. Use environment variables or a .env file in development and secret managers in production.

Future Enhancements
Add filters for state, gender, income group, etc.

Multilingual support (e.g., Hindi, Marathi)

Real-time integration with data.gov.in

User-friendly UI with chat history and PDF export
