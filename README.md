# 🎵 SonicSense AI — Music Genre Classification

**Python · TensorFlow · CNN · FastAPI · Librosa**

SonicSense AI is an end-to-end **Deep Learning application for automatic music genre classification**. It analyzes audio tracks, converts them into **Mel Spectrograms**, and uses a **Convolutional Neural Network (CNN)** to classify music into genres such as Rock, Jazz, Hip-Hop, Classical, and more.

The project provides a complete machine-learning pipeline:

**Audio Processing → 10 × 3-second Audio Slices → Mel Spectrogram (128 × 130) → CNN Model → Genre Prediction → FastAPI Backend → Interactive Web Interface**

---

## ✨ Features

* 🎧 **Audio Processing** — Converts raw audio into Mel Spectrograms using `Librosa`.
* 🧠 **CNN-Based Classification** — Custom Convolutional Neural Network trained on the GTZAN dataset.
* ⚡ **FastAPI Backend** — High-performance REST API for serving model predictions.
* 🖥️ **Modern Frontend** — Responsive UI with drag-and-drop audio upload and animated visual effects.
* 📊 **Confidence Scores** — Displays the predicted genre along with the model's confidence.
* 🔄 **End-to-End Pipeline** — Integrates data preprocessing, model training, inference, API serving, and frontend interaction.

---
## 📸 Project Demo

<p align="center">
  <img width="700" alt="Classical genre result" src="https://github.com/user-attachments/assets/1a23baf0-cf34-4370-a1bb-fad9f788e22d" />
</p>
<p align="center">
  <img width="700" alt="Rock genre result" src="https://github.com/user-attachments/assets/22e444f6-c8e2-421f-883f-d144a04620d6" />
</p>


Example:

```text
Frontend Interface
Audio Upload → Model Prediction → Genre + Confidence Score
```

---

## 📂 Project Structure

```text
Music-Genre-AI-Project/
│
├── 📓 music_genre_solution.ipynb   # Model training & preprocessing
├── 📜 requirements.txt             # Python dependencies
│
├── 📂 backend/
│   ├── main.py                     # FastAPI application
│   └── 📂 model/
│       └── music_genre_cnn.keras    # Trained CNN model
│
└── 📂 frontend/
    ├── index.html                  # Main UI
    ├── style.css                   # Styling & animations
    └── script.js                   # Frontend/API interaction
```

---

## 🚀 How to Run Locally

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/Music-Genre-AI-Project.git
cd Music-Genre-AI-Project
```

### 2. Install Dependencies

Make sure Python is installed on your system.

```bash
pip install -r requirements.txt
```

---

### 3. Train the Model

The trained model is not included in the repository because of its large file size.

Open:

```text
music_genre_solution.ipynb
```

Run all cells in the notebook.

The notebook will generate:

```text
music_genre_cnn.keras
```

Move the generated model into:

```text
backend/model/music_genre_cnn.keras
```

---

### 4. Start the FastAPI Backend

Navigate to the backend directory:

```bash
cd backend
```

Start the server:

```bash
python -m uvicorn main:app --reload
```

The backend should start successfully and load the trained model.

---

### 5. Launch the Frontend

Open the following file in **Chrome or Microsoft Edge**:

```text
frontend/index.html
```

Upload an audio file using the drag-and-drop interface.

The application will process the audio and return:

```text
Predicted Genre
Confidence Score
```

🎧 **Upload → Analyze → Get Genre Prediction**

---

## 📊 Dataset

The model is trained using the **GTZAN Genre Collection**, a commonly used dataset for music genre classification.

The dataset contains **1,000 audio tracks**, with each track approximately **30 seconds** long.

### 🎼 Supported Genres

| Genre     |
| --------- |
| Blues     |
| Classical |
| Country   |
| Disco     |
| Hip-Hop   |
| Jazz      |
| Metal     |
| Pop       |
| Reggae    |
| Rock      |

---

## 🧠 Machine Learning Pipeline

The project uses an audio-slicing and Mel Spectrogram-based CNN pipeline:

```text
GTZAN Audio Track (30 seconds)
            ↓
     Split into 10 slices
            ↓
     3-second Audio Slices
            ↓
      Mel Spectrogram
            ↓
        128 × 130
            ↓
      Add Channel Dimension
            ↓
       128 × 130 × 1
            ↓
           CNN
            ↓
    10 Genre Classification
            ↓
     Confidence Score
            ↓
        FastAPI API
            ↓
     Interactive Web UI
```

### Why Mel Spectrograms?

A Mel Spectrogram represents the frequency content of an audio signal over time while using a frequency scale that better reflects human auditory perception.

This allows the CNN to treat audio features as a visual representation and learn meaningful patterns associated with different musical genres.

---

## 🛠️ Tech Stack

### Programming Language

* Python

### Machine Learning / Deep Learning

* TensorFlow
* Keras
* NumPy
* Scikit-learn

### Audio Processing

* Librosa

### Backend

* FastAPI
* Uvicorn

### Frontend

* HTML5
* CSS3
* JavaScript
* Fetch API

---

## 🔮 Future Improvements

* 🎵 Add support for longer audio tracks.
* 📈 Improve model accuracy through data augmentation.
* 🤖 Experiment with transfer-learning architectures.
* 🎼 Add top-3 genre predictions.
* 📊 Add audio waveform and spectrogram visualization.
* ☁️ Deploy the application using a cloud platform.
* 📱 Improve mobile responsiveness.
* ⚡ Optimize inference speed for real-time predictions.

---

## 👨‍💻 Author

**Ayush**

Developed as an end-to-end **Deep Learning + FastAPI + Web Development** project for automatic music genre classification.

---

## ⭐ If You Like This Project

If you find this project useful or interesting, consider giving the repository a ⭐ on GitHub!
