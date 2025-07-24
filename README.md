# Career Conversation Chatbot

This project is an interactive, AI-powered chatbot designed to act as your digital representative. It answers questions about your career, skills, and experience based on your personal data, such as a LinkedIn profile or resume. Built with Gradio, Google Gemini, and the OpenAI Python library, it creates a personal and engaging experience for visitors to your website or portfolio.

The chatbot is equipped with function-calling capabilities to record questions it cannot answer and capture contact details from interested users, ensuring you never miss an opportunity.

## Features

* Personalized AI Persona: The chatbot adopts your persona, using provided PDF and text files (like your resume or a personal summary) as its knowledge base.
* Intelligent Tool Use:
    * Records Unknown Questions: If the chatbot can't answer a question, it uses a tool to log the query so you can review it later.
    * Record User Details: It can identify when a user is interested in getting in touch and will prompt for their email, recording the details for follow-up.
* Easy to Deploy: Can be run locally or deployed easily to services like Hugging Face Spaces.
* Real-time Notifications: Integrates with Pushover to send you instant notifications for new questions or captured leads.

## Technical Stack

* Language: Python
* AI Model: Google Gemini(`Gemini-2.0-flash`)
* Framework: Gradio for web interface
* Libraries: OpenAI (integration with Gemini), PyPDF, python-dotenv, gradio

## Setup and Installation

1. Clone the repository
```
git clone https://github.com/danish0511/career_conversation_chatbot.git
cd career_conversation_chatbot
```

2. Install dependencies
```
uv init                                 # for initializing uv
uv venv                                 # create virtual environment
uv pip install -r requirements.txt      # for installing requirements
```

3. Prepare your data
* `Profile.pdf`: Add your resume or LinkedIn profile export in PDF format to the root directory.
* `Profile.txt`: Create a text file containing a summary or any additional information you want the chatbot to know.

4. Configure environment variable
```
# Get from Google AI Studio
GEMINI_API_KEY="YOUR_GEMINI_API_KEY"

# Get from your Pushover account
PUSHOVER_TOKEN="YOUR_PUSHOVER_APP_TOKEN"
PUSHOVER_USER="YOUR_PUSHOVER_USER_KEY"
```

5. To run the application
```
uv run app.py
```

6. To deploy run given command and use hugging face token to connect
```
gradio deploy
```
