⚡ Action Item Extractor (AI-Powered)

A serverless, browser-based productivity tool that transforms unstructured meeting transcripts into structured, actionable tasks.

🚀 Project Overview

In fast-paced work environments, crucial action items often get lost in the noise of long meetings. This project solves that problem by leveraging Generative AI to analyze natural language (text or voice) and extract structured data: Task Description, Owner, and Deadline.

Key Differentiator: Unlike traditional apps that require heavy backend servers, this prototype runs entirely client-side. It demonstrates how modern Frontend Engineering can interface directly with powerful LLMs to build fast, privacy-focused tools with zero server latency.

✨ Key Features

-🤖 Smart AI Extraction: Uses Google Gemini 2.0 Flash with strict prompt engineering to force structured JSON output from chaotic natural language.

-🎙️ Live Dictation: Integrates the Web Speech API for real-time speech-to-text transcription (supports "Sticky Recording" to keep listening during pauses).

-📂 Multi-Modal Input: Supports manual text entry, .txt file uploads (via FileReader API), and voice dictation.

-🎨 Glassmorphic UI: A polished, modern interface built with Tailwind CSS, featuring translucent panels, animated background blobs, and responsive interactions.

-💾 Smart Persistence: Uses localStorage to securely cache API credentials, offering a seamless "login-free" experience for the user.

-🔄 Multi-Session Workflow: Allows appending tasks from back-to-back meetings without losing previous context.

🛠️ Tech Stack

-Core: HTML5, Vanilla JavaScript (ES6+)

-Styling: Tailwind CSS (Utility-first framework for rapid, responsive design)

-AI Model: Google Gemini 2.0 Flash (via Google Generative Language REST API)

-Browser APIs:

  Web Speech API (for Dictation)

  FileReader API (for File Uploads)

  LocalStorage API (for Persistence)

  Clipboard API (for Exporting)

🧠 Technical Highlights

1. Robust JSON Parsing Logic

LLMs can sometimes be unpredictable. To ensure application stability, I implemented a robust parsing mechanism using Regex (match(/\[.*\]/s)). This isolates the JSON array from any conversational filler text the AI might generate, ensuring the UI never crashes due to malformed data.

2. Serverless "BYOK" Architecture

This project implements a "Bring Your Own Key" (BYOK) architecture. By calling the AI API directly from the client, I eliminated the need for a Node.js/Python backend. This reduces hosting costs to zero and improves latency, as data doesn't have to hop through an intermediate server.

3. Asynchronous State Management

The application handles complex asynchronous flows—waiting for AI responses, managing microphone streams, and reading files—while maintaining a responsive UI with loading states, toast notifications, and error handling.

🚀 How to Run

-Clone this repository.

-Open index.html in any modern browser (Chrome, Edge, or Safari recommended for Speech API support).

-On the first run, the app will ask for a Gemini API Key (or use the embedded demo mode).

-Start typing, uploading, or speaking to extract tasks!

🔮 Future Roadmap

-Export Integrations: Add functionality to send tasks directly to Jira, Trello, or Notion APIs.

-Speaker Diarization: Implement logic to automatically distinguish between different speakers in the transcript.

-PWA Support: Convert the application into a Progressive Web App for mobile installation.

Built with ❤️ and code by Sufiyan
