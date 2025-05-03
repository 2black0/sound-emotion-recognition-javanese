# 🗣️ Sound Emotion Recognition — Javanese Speech Dataset

This repository contains a custom **Javanese-language speech emotion recognition (SER)** dataset along with preprocessing, feature extraction, and machine learning code for recognizing emotions from audio. It supports six distinct emotional categories expressed through spoken utterances by ten speakers.

---

## 🎯 Objectives

* Develop an audio-based emotion classification system in **Javanese**
* Provide a reproducible and scalable **open dataset**
* Enable training of **machine learning and deep learning** models
* Advance low-resource language research in speech processing

---

## 📁 Project Structure

```
.
├── code/
│   ├── sound-emotion-recognition-javanese.ipynb   # Main notebook (feature extraction, model training)
│   └── model/
│       ├── final_model.sav                        # Trained model (classical)
│       ├── final_model_NeuralNetwork.sav          # Trained model (MLP/NN)
│       ├── x_train.npy, y_train.npy               # Training dataset (MFCC + labels)
│       ├── x_test.npy, y_test.npy                 # Test dataset (MFCC + labels)
├── dataset/
│   ├── dataset-person-01.zip ... dataset-person-10.zip  # Per-speaker WAV files
│   └── How-To-Read-The-Dataset.txt               # Dataset naming guide
├── LICENSE
└── README.md
```

---

## 🧠 Dataset Description

Each file in the dataset follows the naming convention:

```
aa-bb-cc-dd.wav
```

| Code | Meaning           | Range | Description                        |
| ---- | ----------------- | ----- | ---------------------------------- |
| `aa` | Actor ID          | 01–10 | 10 speakers (Javanese male/female) |
| `bb` | Sentence ID       | 01–04 | 4 predefined spoken sentences      |
| `cc` | Emotion Category  | 01–06 | See emotion list below             |
| `dd` | Repetition Number | 01–07 | 7 repetitions per sentence-emotion |

### Emotion Labels:

| Code | Emotion   | Label ID |
| ---- | --------- | -------- |
| 01   | Neutral   | 0        |
| 02   | Sadness   | 1        |
| 03   | Happiness | 2        |
| 04   | Surprise  | 3        |
| 05   | Fear      | 4        |
| 06   | Anger     | 5        |

📌 Example:

```
01-02-03-04.wav → Actor 01, Sentence 2, Emotion: Happiness, Repetition 4
```

---

## 🧪 Model Training

The included Jupyter Notebook performs:

1. **Audio Preprocessing**: Sampling, padding, trimming
2. **Feature Extraction**: MFCC, Delta, Zero-Crossing Rate
3. **Modeling**:

   * Classical (e.g., RandomForest, SVM)
   * Neural Network (MLP using `sklearn`)
4. **Evaluation**: Accuracy, Confusion Matrix

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/sound-emotion-recognition-javanese.git
cd sound-emotion-recognition-javanese
```

### 2. Install Dependencies

Make sure you have Python 3.8+ installed. Then install required packages:

```bash
pip install numpy scipy librosa matplotlib scikit-learn joblib
```

### 3. Run Notebook

Open the notebook with Jupyter:

```bash
jupyter notebook code/sound-emotion-recognition-javanese.ipynb
```

Or convert it to a script:

```bash
jupyter nbconvert --to script code/sound-emotion-recognition-javanese.ipynb
```

---

## 📦 Model Files

| File                            | Description                        |
| ------------------------------- | ---------------------------------- |
| `final_model.sav`               | Classical ML model (e.g. SVM/Tree) |
| `final_model_NeuralNetwork.sav` | Neural Network-based model (MLP)   |
| `x_train.npy`, `y_train.npy`    | Numpy array for training           |
| `x_test.npy`, `y_test.npy`      | Numpy array for testing            |

---

## 🗃️ Potential Applications

* Assistive technology for emotion-aware interaction
* Language-specific emotion analytics in Javanese
* Low-resource multilingual SER benchmarking
* Voice-controlled educational platforms

---

## 📜 License

This project is licensed under the [MIT License](LICENSE) — free to use, modify, and distribute.

---

## 👨‍💻 Author

Developed by [2black0](mailto:2black0@gmail.com)

---