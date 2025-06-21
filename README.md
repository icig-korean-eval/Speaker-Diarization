# 🎙️ Speaker Diarization System

This project implements and evaluates a speaker diarization system using a multi-speaker Korean speech dataset provided by AI Hub.

## 📂 Dataset

- **Source**: [AI Hub - Foreigners' Korean Speech Dataset](https://aihub.or.kr/aihubdata/data/view.do?currMenu=115&topMenu=100&aihubDataSe=data&dataSetSn=71631)
- **Description**: The dataset contains Korean speech spoken by non-native speakers from various language backgrounds, along with transcription and metadata.
- **Usage**: It is used for speaker diarization and pronunciation evaluation tasks.

## 🧠 Model & Tech Stack

- **Model**: Pretrained diarization model from `pyannote.audio` (e.g., `pyannote/speaker-diarization@2.1`)
- **Frameworks & Libraries**: Python, PyTorch, Jupyter Notebook, torchaudio
- **Main Components**:
  - Audio preprocessing
  - Inference using pyannote diarization pipeline
  - Visualization and evaluation of diarization results

## ⚠️ Known Issues

- **Poor separation between same-gender speakers**:  
  The model struggles to distinguish between speakers of the same gender (e.g., male-male or female-female), due to acoustic similarities such as pitch range and speech tempo.

- **Root Causes**:
  - Embedding space lacks sufficient discriminative power for same-gender speaker separation.
  - Pretrained model is not fine-tuned on the target domain or language.

- **Suggested Improvements**:
  - Apply better clustering techniques on speaker embeddings.
  - Fine-tune the diarization model using in-domain Korean data.
  - Incorporate additional speaker-specific acoustic features (e.g., prosody, articulation rate).


## 🔖 References

- [pyannote.audio GitHub](https://github.com/pyannote/pyannote-audio)
- [AI Hub Korean Speech Dataset](https://aihub.or.kr/aihubdata/data/view.do?currMenu=115&topMenu=100&aihubDataSe=data&dataSetSn=71631)

---
