# College Enquiry Chatbot

An intent-classification chatbot (Flask backend + TensorFlow/Keras model) that answers common college-enquiry questions — courses, semesters, requirements, etc. — trained on a small labeled intents dataset.

> **Attribution:** This project is based on/adapted from a college project originally authored by **Riya Nakarmi** (credited directly in the source comments of `main.py` and `trainingData.py`). It's kept here as a study project for learning intent-classification chatbots with NLTK/TensorFlow/Flask, not as original work.

## How it works

1. `trainingData.py` builds a bag-of-words vocabulary from `intents.json`, trains a small Keras neural network to classify user messages into an intent tag, and saves `chatbotmodel.h5`, `words.pkl`, `classes.pkl`.
2. `main.py` runs a Flask server that loads the trained model, classifies incoming messages, and returns a random response for the predicted intent.

## Tech stack

Flask, TensorFlow/Keras, NLTK, NumPy

## Getting started

```bash
cd "AI_Chatbot_In_Python_JavaScript/AI chatbot"
python -m venv .venv
source .venv/Scripts/activate   # Windows
# source .venv/bin/activate     # macOS/Linux

pip install -r requirements.txt

# (optional) retrain the model on intents.json
python trainingData.py

python main.py
```

Then open `http://localhost:5000`.

## License

MIT (this adaptation) — see attribution note above for the original source material.
