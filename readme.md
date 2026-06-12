# PyMentor - Your Personal AI Python Tutor

PyMentor is a customized, production-ready AI agent engineered specifically to act as a warm, encouraging, and highly patient coding mentor for absolute programming beginners. 

Unlike standard conversational models, PyMentor is uniquely constrained to focus entirely on software development education, employing analogies over spoon-feeding answers, and breaking down syntax barriers securely.

> **Project Origin:** This application was developed as a hands-on technical project during the **Microsoft AI Skills Fest 2026**, utilizing Microsoft Azure AI Foundry capabilities alongside a Python Flask backend client.

---

## Project Demonstration
See PyMentor in action! The demo below highlights the custom prompt engineering rules handling real-time beginner errors, generating clean code blocks, and staying strictly on track using guardrails:


https://github.com/user-attachments/assets/80003e59-6d28-448f-abd3-29538b3363ca


---

## Key Features

* **Empathetic Debugging Logic:** Programmed to guide users through *why* syntax and logic errors occur in plain English, ensuring foundational learning over automated code generation.
* **Concept Simplification:** Automatically maps abstract programming concepts (like lists, variables, and loops) to concrete, digestible real-world analogies.
* **Intelligent Scope Guardrails:** Built-in safeguards reject off-topic or irrelevant queries, keeping the user interface completely focused on technical development.
* **Smart Memory Tracking:** Tracks conversation history dynamically to allow seamless, context-aware follow-up questions during troubleshooting sessions.

---

## Core Architecture

The system is split into two cleanly separated layers:
1. **Frontend/Backend Web Client:** A Python-based Flask application (`app.py`) providing a streamlined browser user interface.
2. **AI Engine Agent:** A modularized agent handler (`agent_client.py`) that formats context, manages prompt parameters, and interfaces with Microsoft Azure AI infrastructure.

---

## Local Setup & Installation

To run PyMentor locally, you will need Python 3.10+ installed on your machine.

# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git

# 2. Step into the application folder
cd YOUR_REPOSITORY_NAME/computer-history-client

# 3. Create a virtual environment
python -m venv .venv

# 4. Activate the virtual environment

# On Windows:
.venv\Scripts\activate

# On Mac/Linux:
source .venv/bin/activate

# 5. Install the required Python packages
pip install -r requirements.txt
Environment Configuration

Create a .env file inside the computer-history-client folder (you can use the provided .env.example file as a template).

Add your Microsoft AI endpoint credentials securely:

AGENT_ENDPOINT="your_microsoft_foundry_endpoint_here"
Note on Subscription Expiration (Mock Mode)

If the live Azure endpoint is currently offline or the trial subscription has lapsed, the application includes an offline fallback mode.

Simply add the following to your .env file:

MOCK_MODE=true

This allows you to explore the frontend user interface and application routing logic without requiring active API keys.

Running the Application

Once your environment is configured, launch the local web server by executing the primary Flask script:

python app.py

Open your web browser and navigate to:

http://127.0.0.1:5000

to start your session with PyMentor.
