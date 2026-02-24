# 🎙️ The Empathy Engine

## *Giving AI a Human Voice*

The Empathy Engine is an emotion-aware Text-to-Speech (TTS) service that
dynamically adjusts vocal characteristics based on the detected emotion
of input text.

It enhances traditional robotic TTS systems by introducing expressive,
human-like voice modulation.

------------------------------------------------------------------------

# ✨ Features

## 🔍 Emotion Detection

The engine analyzes input text and detects:

### Base Sentiment

-   **Positive**
-   **Negative**
-   **Neutral**

### Granular Emotional States

-   **Surprised**
-   **Inquisitive**
-   **Concerned**

------------------------------------------------------------------------

## 🎚 Dynamic Voice Modulation

The system adjusts:

-   **Speech Rate**
-   **Volume**

### Emotional Personas

-   **Positive** → Fast, energetic\
-   **Negative** → Very slow, soft\
-   **Surprised** → Rapid, louder\
-   **Concerned** → Slow, soft\
-   **Inquisitive** → Slightly faster, engaging\
-   **Neutral** → Balanced and steady

------------------------------------------------------------------------

## 🎤 Smart Voice Selection

The system attempts to automatically select a more empathetic female
voice (e.g., **"Zira"** on Windows), if available.

------------------------------------------------------------------------

## 🌐 Web Interface

-   Simple and clean UI
-   Enter text
-   Analyze emotion
-   Generate expressive speech instantly

------------------------------------------------------------------------

## 💻 CLI Support

``` bash
python cli.py "I am so happy to see you!"
python cli.py "This is really frustrating."
```

------------------------------------------------------------------------

# 📦 Prerequisites

-   Python 3.8+
-   Windows (Recommended for `pyttsx3` voice support)
-   macOS or Linux (also supported)

------------------------------------------------------------------------

# ⚙️ Setup

## 1️⃣ Navigate to Project Directory

``` bash
cd empathy_engine
```

## 2️⃣ Create and Activate Virtual Environment

### Windows

``` bash
python -m venv venv
venv\Scripts\activate
```

### macOS/Linux

``` bash
python3 -m venv venv
source venv/bin/activate
```

## 3️⃣ Install Dependencies

``` bash
pip install -r requirements.txt
```

------------------------------------------------------------------------

# 🚀 Usage

## 🌐 Web Interface

``` bash
python main.py
```

Open your browser:

http://localhost:8000

------------------------------------------------------------------------

## 💻 CLI Mode

``` bash
python cli.py "I am so happy to see you!"
```

------------------------------------------------------------------------

# 🧠 Design Choices

## Emotion Analysis

-   Uses `vaderSentiment` for sentiment polarity scoring.
-   Applies heuristic rules (punctuation, keywords) to detect nuanced
    emotions like surprise and concern.

## TTS Engine

`pyttsx3` was selected because:

-   Works fully offline
-   No API key required
-   Cross-platform support
-   Stable control over speech rate and volume

## Modulation Logic

-   **Rate** conveys emotional energy (fast = excitement, slow =
    concern).
-   **Volume** enhances emotional tone (loud = surprise, soft = worry).

This parameter-based modulation ensures consistent playback without
relying on unstable SSML implementations.

------------------------------------------------------------------------

# 🛠 Troubleshooting

-   **No Audio** → Check system volume.
-   **Module Not Found** → Activate virtual environment and ensure
    correct directory.

------------------------------------------------------------------------

# 🧪 Example Inputs

-   "I cant, I am so worried about this situation."
-   "Wait, really? That happened?"
-   "Oh my god! That is amazing!"
-   "Why would they do that?"
-   "This is the best news ever!"

------------------------------------------------------------------------

# 🎯 Conclusion

The Empathy Engine demonstrates how AI can move beyond functional speech
synthesis and incorporate emotional intelligence into voice interaction.
