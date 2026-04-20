## 📌 Overview
This project implements an end-to-end pipeline for processing code-switched Hindi-English speech.

It integrates:
- Language Identification (LID)
- Speech-to-Text (STT)
- IPA Conversion
- Translation
- Prosody Analysis (DTW)
- Adversarial Testing

---

## 🚀 Features
- BiLSTM-based Language Identification
- Whisper-based Speech Recognition
- IPA Conversion using G2P
- Dictionary-based Translation
- DTW-based Prosody Alignment
- FGSM Adversarial Testing
- Graph Outputs (Confusion Matrix, DTW Plot)

---

## 🧠 Pipeline
Audio → Denoise → MFCC → LID → STT → IPA → Translation → TTS → DTW → Adversarial

---

## 📂 Project Structure
project/
│
├── notebook.ipynb
├── confusion_matrix.png
├── dtw_plot.png
├── README.md
├── requirements.txt
│
└── data/
    ├── original_segment.wav
    └── student_voice_ref.wav

---

## ⚙️ Installation
pip install -r requirements.txt

---

## ▶️ Usage
1. Open notebook
2. Mount Google Drive
3. Set paths:

INPUT_AUDIO = "/content/drive/MyDrive/original_segment.wav"
VOICE_SAMPLE = "/content/drive/MyDrive/student_voice_ref.wav"

4. Run all cells

---

## 📊 Outputs
- Transcript
- F1 Score
- WER
- IPA Output
- Translated Text
- confusion_matrix.png
- dtw_plot.png

---

## ⚠️ Limitations
- Dummy labels used for LID
- Translation is rule-based
- TTS is simulated

---

## 🏁 Conclusion
This project demonstrates a complete speech pipeline for code-switched input using ML and DSP techniques.

---

## 👤 Author
Your Name
Roll Number
"""

# ================= requirements.txt =================
requirements = """librosa
numpy
matplotlib
jiwer
dtw-python
soundfile
g2p_en
openai-whisper
scikit-learn
scipy
nltk
torch
"""

# ================= SAVE FILES =================
with open("README.md", "w") as f:
    f.write(readme)

with open("requirements.txt", "w") as f:
    f.write(requirements)

print("README.md and requirements.txt created successfully!")
