🧠 AI-Powered Research Assistant
Chrome Extension + Spring Boot Backend Integration








📋 Overview

The AI-Powered Research Assistant is a browser extension designed to make online reading and research more efficient.
With just a click, the extension captures selected text from any webpage and sends it to a Spring Boot backend powered by AI summarization APIs (e.g., Gemini API).

The backend processes and returns a concise summary — helping users quickly understand complex information without leaving the page.

🚀 Key Features

🔍 Smart Summarization: Highlights and summarizes webpage text in real time.

🔗 Chrome Extension UI: Lightweight popup interface for quick interactions.

⚙️ Spring Boot Backend: Handles API requests and AI-based text summarization.

🌐 Cross-Origin Support (CORS): Seamless communication between frontend and backend.

💾 Notes Saving (optional): Allows storing summaries locally or on the server.

🔐 Environment Variable Support: Keeps API keys secure and configurable.

🏗️ Architecture
[ User ] ──► [ Chrome Extension (Frontend) ]
                    │
                    ▼
        [ Spring Boot Backend (API Layer) ]
                    │
                    ▼
          [ AI Summarization Engine (Gemini API) ]

🧩 Tech Stack
Frontend (Chrome Extension)

HTML5, CSS3, JavaScript (Vanilla)

Chrome Extension APIs (manifest.json)

Popup UI + Content Scripts

Backend (Spring Boot)

Java 17+

Spring Boot 3.x

WebClient for API calls

Lombok for cleaner code

REST Controller + CORS configuration

⚙️ Installation & Setup
🔹 Step 1: Clone the repository
git clone https://github.com/Kuldeepch13/RESEARCH-ASSISTANT.git
cd RESEARCH-ASSISTANT

🔹 Step 2: Run the Spring Boot backend

Open the project in VS Code or IntelliJ.

Make sure you have Java 17+ and Maven installed.

Add your API key in application.properties:

gemini.api.url=https://api.gemini.ai/v1/summarize
gemini.api.key=YOUR_API_KEY


Run:

./mvnw spring-boot:run


The backend will start on:
👉 http://localhost:8080/api/research/process

🔹 Step 3: Load Chrome Extension

Open Chrome → Extensions → Manage Extensions.

Enable Developer Mode.

Click Load unpacked.

Select the folder:

/RESEARCH-ASSISTANT/extension/


The extension icon should now appear in your Chrome toolbar.

🧠 Usage

Highlight text on any web page.

Click the Research Assistant Chrome Extension icon.

The selected text is automatically sent to your backend.

The AI model summarizes the content and returns the result instantly.

📂 Project Structure
RESEARCH-ASSISTANT/
│
├── src/main/java/com/research_assistant/
│   ├── ResearchController.java       # REST endpoint for summarization
│   ├── ResearchService.java          # Calls Gemini API
│   ├── ResearchRequest.java          # Request DTO
│   ├── GeminiResponse.java           # Response model
│   └── ResearchAssistantApplication.java
│
├── extension/
│   ├── manifest.json                 # Chrome extension manifest
│   ├── popup.html                    # UI for extension
│   ├── popup.js                      # Handles user actions
│   ├── content.js                    # Injected into web pages
│   └── style.css                     # Popup styles
│
├── pom.xml                           # Maven project file
├── .gitignore
└── README.md

🔑 Environment Variables
Variable	Description	Example
GEMINI_API_URL	API endpoint for Gemini summarization	https://api.gemini.ai/v1/summarize
GEMINI_API_KEY	Your Gemini API key	sk-xxxxxxx
📈 Future Improvements

🧩 Support multiple AI models (Gemini, OpenAI, Claude)

💾 Add user authentication and history tracking

🧠 Add "Research Notes" dashboard in extension

🌍 Multi-language summarization support

🎨 Improved UI with dark/light modes

🧑‍💻 Author

Kuldeep Chaudhary
📧 dc629753@gmail.com

🔗 GitHub: Kuldeepch13

🔗 LinkedIn: Kuldeep Chaudhary

📜 License

This project is licensed under the MIT License – see the LICENSE
 file for details.

❤️ Acknowledgements

Google Gemini API

Spring Boot

Chrome Extensions Documentation

Inspiration from real-world research productivity tools.