# rock_paper_scissors_game
🎮 AI-Based Rock Paper Scissors Game
An interactive Rock-Paper-Scissors game that combines classical AI with modern web and machine learning technologies. Playable using both button clicks and real-time hand gesture recognition via webcam.

🚀 Features
🤖 AI opponent using a Markov Chain prediction model

🖱️ Button-based gameplay and ✋ gesture recognition via TensorFlow.js

🔊 Real-time voice feedback using the SpeechSynthesis API

📊 Game statistics tracking

💾 Persistent AI learning using a local JSON model

🧰 Technologies Used
Function	Tool/Library
Backend Server	Flask (Python)
AI Model	Markov Chain (JSON-based persistence)
Frontend Styling	Tailwind CSS
Gesture Detection	TensorFlow.js Handpose
ML in Browser	TensorFlow.js (Core + WebGL backend)
Voice Feedback	Browser SpeechSynthesis API

🔧 Project Structure
🖥️ Backend (app.py)
Built with Flask

Core API routes:

/ – Main game UI

/play – Accepts user move, predicts AI move, returns result

/statistics – Returns overall game stats

/exit – Saves Markov model to model.json

🧠 AI Logic (random_ai.py)
Implements:

Move prediction with a Markov Chain

Game rules and winner determination

Persistent model updates and statistics generation

🌐 Frontend (templates/index.html, static/js/router.js)
Tailwind CSS UI with responsive design

Real-time webcam access for gesture input

Integration of TensorFlow.js Handpose for gesture classification

Dynamic updates for results and statistics

Voice narration of game results

📄 Sample model.json
json
Copy
Edit
{
  "rock": {
    "rock": 3,
    "paper": 2,
    "scissors": 1
  },
  "paper": {
    "rock": 1,
    "paper": 4,
    "scissors": 2
  },
  "scissors": {
    "rock": 2,
    "paper": 3,
    "scissors": 5
  }
}
This model represents the frequency of the player's next move, based on their previous move. The AI uses this to make predictions.

🎥 Demo

(Optional: Add a link to a video demo here)
Live preview: YouTube Demo

📦 Installation
Requirements
Python 3.8+

pip (Python package installer)

Clone the repository
bash
Copy
Edit
git clone https://github.com/yourusername/rock-paper-scissors-ai.git
cd rock-paper-scissors-ai
Set up virtual environment (optional but recommended)
bash
Copy
Edit
python -m venv venv
# Activate environment
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install dependencies
bash
Copy
Edit
pip install -r requirements.txt
Run the app
bash
Copy
Edit
python app.py
Then open your browser and navigate to:
http://127.0.0.1:5000

🎯 How to Play
Choose your move using:

Click buttons (Rock, Paper, Scissors), or

Use your hand gesture via webcam

The AI will predict and counter your move based on previous rounds.

Results, statistics, and voice feedback are displayed instantly.

📈 Future Improvements
Multiplayer mode (co-op or competitive)

Adaptive difficulty adjustment

Gesture-only mode

Augmented Reality (AR) gameplay

Social sharing, leaderboards, and achievements

📝 License
MIT License – feel free to fork, improve, and share!

🙌 Credits
Created as a minor project using Flask, TensorFlow.js, and Markov Chains.
Inspired by a blend of classical game theory and modern AI applications.
