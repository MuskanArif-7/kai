# KAI AI Chatbot

## Project Overview

KAI is a web-based Large Language Model (LLM) chatbot powered by the Groq API. It has a custom animated frontend and allows users to send messages and receive AI-generated replies.

The project uses HTML, CSS, and JavaScript for the frontend, while a Vercel serverless function securely communicates with the Groq API.

## Features

- Custom animated chatbot interface
- User message input and send button
- Conversation history
- AI-generated responses using Groq
- Streaming replies
- Secure API key handling
- Responsive design
- Public deployment through Vercel
- Automatic redeployment through GitHub

## Technologies Used

- **Frontend:** HTML, CSS, and JavaScript
- **Backend:** Vercel Serverless Function
- **LLM Provider:** Groq API
- **Hosting:** Vercel
- **Version Control:** Git and GitHub

## Project Structure

```text
vercel-chatbot/
│
├── api/
│   └── chat.js
├── index.html
├── style.css
├── script.js
├── package.json
├── .gitignore
└── README.md
```

## File Description

- **index.html:** Contains the structure of the chatbot page.
- **style.css:** Contains the chatbot design, layout, colors, and animations.
- **script.js:** Handles user input, sending messages, chat history, and streamed replies.
- **api/chat.js:** Serverless backend function that calls Groq and keeps the API key secret.
- **package.json:** Contains project metadata.
- **.gitignore:** Prevents secret and unnecessary files from being uploaded.
- **README.md:** Provides project and deployment information.

## How the Chatbot Works

1. The user enters a message in KAI.
2. `script.js` sends the message to `/api/chat`.
3. The Vercel serverless function receives the request.
4. The backend calls the Groq API using the secret API key.
5. Groq generates an AI response.
6. The response is streamed back to the browser.
7. KAI displays the reply in the chat window.

## Environment Variable

Create an environment variable named:

```env
GROQ_API_KEY=your_actual_groq_api_key
```

The API key must not be written directly in frontend code or uploaded to GitHub.

## Local Setup

### 1. Download or Clone the Repository

Open the project folder in Visual Studio Code.

### 2. Install Dependencies

If required by the project, run:

```bash
npm install
```

### 3. Add the API Key

Create a `.env` or `.env.local` file and add:

```env
GROQ_API_KEY=your_actual_groq_api_key
```

### 4. Run the Project

For local testing, use:

```bash
npx vercel dev
```

Then open the local URL shown in the terminal.

## Deployment on Vercel

1. Upload all project files to a GitHub repository.
2. Import the repository into Vercel.
3. Select **Other** as the framework preset if required.
4. Open **Project Settings → Environment Variables**.
5. Add:

```text
Name: GROQ_API_KEY
Value: Your Groq API key
```

6. Select Production, Preview, and Development environments.
7. Click **Deploy**.
8. Open the generated public Vercel URL and test KAI.

## Security

The Groq API key is used only inside the backend serverless function. It is not exposed in frontend code.

The following files and folders should not be uploaded to GitHub:

```text
.env
.env.local
node_modules
.vercel
```

Never share your real Groq API key publicly.

## Sample Conversation

**User:** What is artificial intelligence?

**KAI:** Artificial intelligence is a technology that enables computers to perform tasks that normally require human intelligence, such as understanding language, answering questions, recognizing patterns, and making predictions.

## Limitations

- KAI depends on the Groq API and an internet connection.
- API rate limits may affect responses.
- The model may generate incorrect or incomplete information.
- Conversations are not permanently stored unless a database is added.
- KAI should not replace professional advice.

## Future Improvements

- Add a clear-chat button
- Add dark and light themes
- Add multilingual responses
- Add voice input and text-to-speech
- Add user authentication
- Save conversations in a database
- Add better error messages
- Add Retrieval-Augmented Generation (RAG)
- Add custom knowledge from uploaded documents

## Assignment Deliverables

- **Live Vercel URL:** Add your deployed KAI URL here.
- **GitHub Repository URL:** Add your GitHub repository URL here.
- **Sample Conversation Screenshot:** Add a screenshot of the working chatbot here.

## Author

**Name:** Muskan Arif  
**Project:** KAI AI Chatbot  
**Course:** Software Engineering

## Disclaimer

This project is created for educational purposes. KAI generates responses using an AI language model, and its answers should be checked before being used for important decisions.
