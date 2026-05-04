# A-Security-Analysis-of-Tf-Idf-And-Deep-Learning-Model-for-Hate-Speech-Detection-in-YouTube
This repository presents a deep learning-based pipeline for detecting hate speech in YouTube videos by analyzing spoken content. The system combines automatic speech recognition (ASR) and transformer-based text classification to identify harmful language directly from audio.

## 🌐 Live Demo

* 🔗 **Frontend : [vercel](https://hate-speech-detection-jade-eight.vercel.app/)
* ⚙️ **Backend (Colab + ngrok)
---

## 🚀 Features

* 🎥 Extracts audio directly from YouTube videos
* 🧠 Transcribes speech using **Whisper (Large Model)**
* 🗣️ Detects hate speech using **RoBERTa classifier**
* 📊 Provides:

  * Chunk-level predictions
  * Overall classification score
* 🌐 Clean and responsive frontend UI
* 🔗 Real-time API communication with Flask backend

---

## 🧠 Tech Stack

**AI / ML**

* Whisper (Large) – Speech-to-Text
* RoBERTa – Hate Speech Classification

**Backend**

* Flask (REST API)
* ngrok (temporary public tunnel)
* Google Colab (model execution)

**Frontend**

* HTML, CSS, JavaScript
* Deployed on Vercel

**Tools & Libraries**

* PyTorch
* Transformers (Hugging Face)
* yt-dlp (audio extraction)

---

## ⚙️ How It Works

1. User enters a YouTube video URL
2. Backend downloads audio using `yt-dlp`
3. Whisper converts audio → text
4. RoBERTa analyzes text → predicts:

   * Hate
   * Non-hate
5. API returns structured JSON
6. Frontend visualizes:

   * Chunk-level classification
   * Overall probability

---

## 🏗️ System Architecture

```
Whisper Large (ASR)
        ↓
RoBERTa (Classifier)
        ↓
Results 
```

---

## 📡 API Endpoint

**POST /analyze**

### Request:

```json
{
  "url": "https://www.youtube.com/watch?v=..."
}
```

### Response:

```json
{
  "transcription": "...",
  "chunks": [...],
  "overall": {
    "hate_pct": 65.2,
    "nothate_pct": 34.8,
    "verdict": "hate"
  }
}
```

---

## 📦 Setup Instructions

### 🔹 1. Clone Repository

```bash
git clone[https://github.com/sauravv19/A-Security-Analysis-of-Tf-Idf-And-Deep-Learning-Model-for-Hate-Speech-Detection-in-YouTube]
```

---

### 🔹 2. Run Backend (Colab)

* Open the notebook in Google Colab
* Run all cells
* Copy the generated ngrok URL

---

### 🔹 3. Connect Frontend

* Open deployed frontend (Vercel)
* Paste ngrok URL in backend input field

---

### 🔹 4. Analyze

* Paste YouTube link
* Click **Analyze**
* View results

---

## ⚠️ Limitations

* ⏳ **High latency** due to Whisper Large model
* 🔌 Backend is **not persistent** (Colab session required)
* 🔄 ngrok URL changes every run
* 📉 Not optimized for production-scale deployment

---

## 📌 Future Improvements

* ⚡ Model optimization (faster inference)
* ☁️ Deploy backend on cloud (Render / AWS)
* 🎯 Add real-time streaming support
* 📊 Advanced visualization (charts, timelines)
* 🧠 Improve classification accuracy

---

## 👨‍💻 Author

Saurav Kumar
Saharyar Khan
Shah Faisal

---

## 📄 License

This project is for educational and research purposes.

