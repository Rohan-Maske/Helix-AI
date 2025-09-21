# Helix AI Chat Application

![Helix AI](https://img.shields.io/badge/Version-1.0.0-blue.svg) ![License](https://img.shields.io/badge/License-Proprietary-lightgrey.svg) ![Python](https://img.shields.io/badge/Python-3.10%2B-green.svg)

Helix AI is a powerful desktop chat application that provides an interactive interface for users to chat with an advanced AI assistant powered by Groq's API. Built with Python and customtkinter, it offers a modern, terminal-style interface with extensive customization options.

## Features

- 🤖 AI-powered conversations using Groq's advanced language models
- 🔐 Secure user authentication with OTP verification
- 💬 Real-time messaging with message reactions and pinning
- 🎨 Customizable themes and user profiles
- 🔍 Message search functionality
- 📊 Achievement system to track user progress
- ⚙️ Extensive settings customization
- 💾 Automatic chat saving and data persistence

## Prerequisites

Before running Helix AI, ensure you have the following installed:

- Python 3.10
- pip (Python package manager)

## Installation

1. Clone or download the Helix AI application files
2. Navigate to the project directory in your terminal/command prompt
3. Install the required dependencies:

```bash
pip install customtkinter pillow python-dotenv groq
```

## Environment Setup

To use Helix AI, you need to create a `.env` file in the project directory with your specific configuration:

1. Create a new file named `.env` in the main project folder
2. Add the following content to the file, replacing the placeholder values with your actual information:

```
GroqAPIKey = your_groq_api_key_here
Assistantname = Your_Assistant_Name
Username = Your_Username
EMAIL_PASSWORD = your_email_app_password_here
```

### Obtaining Required Credentials

**Groq API Key:**
1. Sign up for an account at [Groq Cloud](https://console.groq.com/)
2. Navigate to the API Keys section
3. Generate a new API key and copy it

**Email Password (for OTP functionality):**
1. Use a Gmail account for sending OTP emails
2. Enable 2-factor authentication on your Gmail account
3. Generate an App Password:
   - Go to your Google Account settings
   - Navigate to Security → 2-Step Verification → App passwords
   - Generate a password for the application
   - Use this generated password as your EMAIL_PASSWORD

## Usage

1. After setting up the `.env` file, run the application:

```bash
python main.py
```

2. The login screen will appear where you can:
   - Register a new account (requires OTP verification)
   - Login to an existing account
   - Reset your password if needed

3. Once logged in, you can:
   - Start new chats with the AI assistant
   - Customize your profile and settings
   - Search through your conversation history
   - React to messages and pin important ones

## Application Structure

- `main.py` - Main application file containing all the UI and logic
- `Database.json` - Automatically created to store user data (created on first run)
- `ChatLog[user_id].json` - Stores conversation history for each user
- `Profiles/` - Directory for user profile pictures
- `Backgrounds/` - Directory for custom chat backgrounds
- `Emails/` - Directory for email logs if SMTP fails

## Troubleshooting

1. **OTP emails not sending**: 
   - Check your EMAIL_PASSWORD in the `.env` file
   - Verify your Gmail account has 2-factor authentication enabled
   - Check the `Emails/` directory for error logs

2. **API errors**:
   - Verify your Groq API key is correct and has sufficient credits
   - Check your internet connection

3. **UI rendering issues**:
   - Ensure you have the latest version of customtkinter
   - Try running on a different Python version if problems persist

## Support

For issues related to:
- API functionality: Check Groq's documentation at https://docs.groq.com/
- UI components: Check customtkinter documentation at https://github.com/TomSchimansky/CustomTkinter
- Application errors: Check the generated log files in the respective directories

## Disclaimer

This application requires a valid Groq API key to function. Users are responsible for any costs associated with API usage according to Groq's pricing model.
