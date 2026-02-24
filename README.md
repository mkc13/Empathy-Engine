The Empathy Engine
Giving AI a Human Voice

The Empathy Engine is an emotion-aware Text-to-Speech (TTS) service that dynamically adjusts vocal characteristics based on the detected emotion of input text. It enhances traditional robotic TTS systems by introducing expressive, human-like modulation.

Features

Emotion Detection

Detects base sentiment: Positive, Negative, Neutral

Detects granular states: Surprised, Inquisitive, Concerned

Dynamic Voice Modulation

Adjusts Speech Rate and Volume

Emotional Personas:

Positive → Fast, energetic

Negative → Very slow, soft

Surprised → Rapid, louder

Concerned → Slow, soft

Inquisitive → Slightly faster, engaging

Neutral → Balanced and steady

Smart Voice Selection

Attempts to select a female voice (e.g., "Zira" on Windows) for a more empathetic tone.

Web Interface

Simple UI to analyze text and generate expressive speech.

CLI Support

Quick emotion analysis and speech generation via terminal.

Prerequisites

Python 3.8+

Windows (Recommended for pyttsx3 voice support), macOS, or Linux

Setup
1. Navigate to Project Directory
cd empathy_engine
2. Create and Activate Virtual Environment
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
3. Install Dependencies
pip install -r requirements.txt
Usage
Web Interface (Recommended)
python main.py

Open your browser and visit:

http://localhost:8000

Enter text and click Analyze or Speak.

CLI
python cli.py "I am so happy to see you!"
python cli.py "This is really frustrating."
Design Choices

Emotion Analysis

Uses vaderSentiment for polarity scoring.

Applies lightweight heuristic rules (punctuation, keywords) to detect nuanced emotions like surprise and concern.

TTS Engine

pyttsx3 selected for:

Offline capability

Cross-platform compatibility

Stable rate and volume control

Modulation Logic

Rate conveys emotional energy (fast = excitement, slow = concern).

Volume enhances emotional tone (loud = surprise, soft = worry).

This parameter-based modulation ensures consistent playback without relying on unstable SSML implementations.

Troubleshooting

No Audio

Check system volume and speaker output.

Module Not Found

Ensure virtual environment is activated.

Ensure you are inside the empathy_engine directory.

Example Inputs

"I cant, I am so worried about this situation."

"Wait, really? That happened?"

"Oh my god! That is amazing!"

"Why would they do that?"

"This is the best news ever!"
