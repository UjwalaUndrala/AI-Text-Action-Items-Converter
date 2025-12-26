# AI Action-Item Converter & Planner
A Smart PWA that turns messy voice transcripts and meeting notes into structured Action Items, Timelines, and Reminders instantly.


## The Problem
In the age of Zoom and remote work, we spend hours in meetings. Afterward, we are left with messy notes, raw transcripts, and the question: "Wait, who was supposed to do what?" Reviewing hour-long recordings to find simple tasks is a waste of productivity.

##  The Solution
AI Action-Item Converter is a lightweight, browser-based tool that:

Listens to your voice or accepts raw text.

Filters out chatter ("Hi", "How are you") and keeps only actionable tasks.

Detects deadlines (Today, Tomorrow, May 30th) and Assignees.

Prioritizes tasks (Red for Urgent, Yellow for Upcoming) automatically.

##  Key Features
###  Instant Voice-to-Text
Uses the Web Speech API with optimized "Live Preview" logic.

No Lag: Text appears instantly as you speak, with additive logic so sentences aren't overwritten.

###  Smart NLP Parsing (Regex Engine)
Chatter Filter: Automatically ignores casual conversation.

Context Awareness: Identifies tasks based on patterns like [Name] to [Task] by [Date].

Date Recognition: Understands absolute dates ("May 30") and relative dates ("Tomorrow", "Next Week").

###  Visual Dashboard
Task Cards: Color-coded based on urgency (🔴 High, 🟡 Medium, 🟢 Low).

Timeline View: Visualizes the schedule of tasks linearly.

Smart Reminders: Set browser notifications for specific tasks directly from the dashboard.

###  One-Click Email Generator
Click any task to auto-generate a formal email to the assignee with the subject and deadline pre-filled.

###  Tech Stack
Frontend: HTML5, CSS3 (Glassmorphism UI).

Logic: Vanilla JavaScript (ES6+).

Voice AI: Web Speech API (Native Browser Support).

Server (Local): Python (http.server) to ensure secure microphone permissions.

Storage: LocalStorage (Privacy-focused, no cloud database required).

##  How to Run Locally
To ensure the Microphone works correctly (browsers often block mic access on file:// paths), please use the included Python launcher.

Clone the Repository:

Bash

git clone https://github.com/HARIPRIYAREDDY98666/AI-Text-Action-Items-Converter.git

cd AI-Text-Action-Items-Converter

Run the Local Server:

Bash

python app.py
Open the App:

The terminal will tell you the URL (usually http://localhost:8000).

Open that link in Google Chrome.

 Sample Inputs to Try
Paste these into the app to see the magic happen!

Scenario 1: Team Meeting (Chat Style)

Rahul: Hi everyone, is the server ready? Rahul: I will fix the login bug by today urgent Priya: Hey, I am working on the designs. Priya: I will submit the logo by May 30th Amit: Is the database updated? Amit to update the schema by next week

Scenario 2: Quick Voice Note

"John to call the client by 5pm today. Sarah will send the report by tomorrow. Team to clean the office."

## Screenshots
<img width="1919" height="905" alt="image" src="https://github.com/user-attachments/assets/915a2a03-ba84-4b21-82a1-79e642ae5db0" />

## Future Improvements
LLM Integration: Connect to Gemini API for summarizing long paragraphs.

Calendar Sync: Add a button to push tasks directly to Google Calendar.

User Accounts: Move from LocalStorage to a cloud database (Firebase).


