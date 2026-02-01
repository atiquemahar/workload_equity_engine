AI Automation Workload Equity Engine
An autonomous logistics and scheduling engine designed to automate teacher coverage assignments. This system replaces manual spreadsheet coordination with an AI-driven process that prioritizes staff workload equity and data integrity.

🚀 Overview
In educational institutions, managing daily teacher absences is a high-friction task. Administrators typically spend 30–60 minutes daily cross-referencing timetables and manually tracking who has covered which class.

The Workload Equity Engine automates this by:

Identifying gaps in the Master Timetable based on absent staff inputs.

Filtering for available (FREE) teachers in real-time.

Using AI to select the best candidate based on historical coverage counts (lowest count first).

Updating the central database and generating a live HTML dashboard for the user.

✨ Key Features
Multi-Teacher Processing: Handles comma-separated inputs (e.g., "John Smith, Mary Johnson") and processes all requirements in a single execution.

Workload Equity Algorithm: Custom JavaScript logic ensures the AI prioritizes teachers with the lowest historical workload to prevent staff burnout.

Automated State Management: Automatically increments "Total Coverages" in the Master Teacher record and appends a detailed audit log to the Coverage History.

Dynamic HTML Feedback: Generates a real-time, scannable response table showing assigned periods, classes, and the AI's reasoning.

🛠️ Tech Stack
Orchestration: n8n

AI Intelligence: OpenAI GPT-4o-mini (Structured JSON Output)

Data Layer: Google Sheets API (Acting as a relational database)

Logic: JavaScript (Preprocessing, Data Synthesis, and Counter Management)

Frontend: HTML/CSS (Dynamic Result Dashboard)

📁 Workflow Structure
Trigger: n8n Form (Production URL).

Data Fetching: Pulls records from Master_Timetable, Teacher_Master, and Coverage_History.

Requirement Extraction: A Code node identifies which classes/periods need covering for the day.

Candidate Filtering: Identifies "Free" teachers and attaches their historical coverage count.

AI Agent: GPT-4o-mini evaluates candidates against the Equity Policy.

Execution: Updates Google Sheets and prepares the final UI response.

⚙️ Setup & Installation
Prerequisites:

An n8n instance (Self-hosted or Cloud).

OpenAI API Key.

Google Cloud Service Account with access to the Google Sheets API.

Installation:

Download the AI_Automation_Workload_Equity_Engine.json file from this repo.

In n8n, click Import from File and select the JSON.

Update the Google Sheets node with your Document ID.

Update the OpenAI node with your credentials.

Spreadsheet Schema:

Ensure your Google Sheet has three tabs: Master_Timetable, Teacher_Master, and Coverage_History with matching headers.

📊 Business Impact
Time Savings: Reduced administrative logistics from 30+ minutes to <5 seconds.

Accuracy: Eliminated human error in data logging and timetable cross-referencing.

Staff Wellbeing: Ensured a 100% transparent and fair distribution of extra work across the teaching faculty.

👤 Author
Atique Ahmed AI Automation Expert 
