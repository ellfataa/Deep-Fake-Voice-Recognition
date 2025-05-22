# 🎙️ Deep Fake Voice Recognition

Sistem deteksi suara deepfake menggunakan machine learning untuk mengidentifikasi apakah audio adalah asli atau hasil manipulasi AI.

## ✨ Fitur Utama

- Deteksi otomatis suara deepfake dengan akurasi tinggi
- Mendukung format .wav dan .mp3
- Visualisasi audio (spektrogram, MFCC, dll)
- Model CNN 1D dan Dense Neural Network
- Confidence score untuk setiap prediksi

## 🛠️ Teknologi

- **TensorFlow/Keras**: Deep learning framework
- **Librosa**: Audio processing dan feature extraction
- **Scikit-learn**: Data preprocessing
- **NumPy, Pandas**: Data manipulation
- **Matplotlib**: Visualisasi

## 🚀 Instalasi

```bash
pip install numpy pandas librosa matplotlib scikit-learn tensorflow
pip install resampy pydub imbalanced-learn tqdm
```

## 🏗️ Arsitektur Model

### CNN 1D Model
```
Input → Conv1D(64,128,256) → BatchNorm → ReLU → MaxPool → Dropout
      → Flatten → Dense(512) → Dense(2) → Softmax
```

### Fitur Audio
- **MFCC**: Mel-frequency Cepstral Coefficients
- **Chroma**: Pitch class profiles  
- **Spectral Contrast**: Valley and peak information
- **Tonnetz**: Tonal centroid features
- **Zero Crossing Rate**: Signal sign changes

## 📊 Dataset

```
dataset/
├── REAL/          # Suara asli
│   └── *.wav
└── FAKE/          # Suara deepfake  
    └── *.wav
```

## ⚠️ Limitasi

- Format: Hanya .wav dan .mp3
- Durasi optimal: 3-30 detik
- Kualitas minimal: 16kHz
- Dataset: Bahasa Inggris

## 📄 Lisensi

MIT License - lihat [LICENSE](LICENSE) untuk detail.
