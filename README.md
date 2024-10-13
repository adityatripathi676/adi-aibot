
# adi-aibot

### A chatbot in python using flask 
---
# AI Bot with API Integration and Local Data Processing

This project implements a simple AI bot that combines responses from an external API with locally processed data. The bot is accessible through a clean, minimalist chat UI running on localhost.

## Features

- Clean, minimalist chat interface
- File upload functionality for local data processing
- Integration with an external API for enhanced responses
- Combination of local and API-based responses

## Project Structure

```
ai_bot_project/
│
├── data/
│   └── uploaded_files/
│
├── static/
│   ├── css/
│   │   └── style.css
│   └── js/
│       └── main.js
│
├── templates/
│   └── index.html
│
├── app.py
├── bot.py
├── api_client.py
├── config.py
├── requirements.txt
└── README.md
```

## Setup and Installation

1. Clone the repository or download the project files.
2. Create a virtual environment:
   ```
   python -m venv venv
   ```
3. Activate the virtual environment:
   - On Windows: `venv\Scripts\activate`
   - On macOS/Linux: `source venv/bin/activate`
4. Install the required packages:
   ```
   pip install -r requirements.txt
   ```
5. Set up your API key:
   - Create an account with the API provider and obtain an API key.
   - Set the API key as an environment variable:
     - On Windows: `set API_KEY=your_api_key_here`
     - On macOS/Linux: `export API_KEY=your_api_key_here`
   - Alternatively, update the `config.py` file with your API key (not recommended for production).

## Running the Application

1. Make sure your virtual environment is activated.
2. Run the Flask application:
   ```
   python app.py
   ```
3. Open a web browser and navigate to `http://localhost:5000`

## Usage

1. Type a message in the chat input and press "Send" to get a response from the bot.
2. Use the file upload feature to add local data for processing.
3. The bot will combine responses based on the uploaded data and the external API.

## File Descriptions

- `app.py`: Main Flask application file that handles routes and requests.
- `bot.py`: Contains the AIBot class, which processes local data and integrates API responses.
- `api_client.py`: Handles communication with the external API.
- `config.py`: Contains configuration settings for the application.
- `index.html`: HTML template for the chat interface.
- `style.css`: CSS file for styling the chat UI.
- `main.js`: JavaScript file for handling chat interactions on the client-side.

## Customization

- To change the API endpoint or other settings, update the `config.py` file.
- Modify the `style.css` file to customize the appearance of the chat interface.
- Extend the `AIBot` class in `bot.py` to add more sophisticated local data processing or response generation.

## Security Considerations

- Always use environment variables to store sensitive information like API keys.
- Implement proper input validation and sanitization for user inputs and file uploads.
- Use HTTPS in production environments to encrypt data in transit.

## Future Improvements

- Implement user authentication and session management.
- Add support for more file types and data processing methods.
- Enhance the UI with features like message history and user preferences.
- Implement more advanced natural language processing techniques for better response generation.
