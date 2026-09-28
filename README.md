# Multi-Modal Deepfake Detection and Source Identification

A multimodal deep learning framework for deepfake detection and source
identity identification using visual, audio, and textual information.

This repository is based on our research project:

**Multi-Modal Solution: Deepfake Detection and the Source Identification**

Published in the Proceedings of the 3rd International Conference on
Public Management and Big Data Analysis (PMBDA 2023).

DOI: 10.4108/eai.15-12-2023.2345299

## Overview

Deepfake detection methods often rely primarily on visual information.
This project explores a multimodal approach that combines information
from three different modalities:

- Visual features
- Audio features
- Text features

The extracted features are fused using a multimodal attention framework
to perform deepfake detection and source identity analysis.

## Architecture

The framework contains four major components:

### Visual Feature Extraction

Video frames are processed using:

- Key-frame extraction based on Sum of Absolute Differences (SAD)
- MTCNN for face detection and localization
- I3D-based feature extraction for temporal visual information

### Audio Feature Extraction

Wav2Vec 2.0 is used to extract representations from raw audio signals
and process speech information.

### Text Feature Extraction

Speech extracted from the audio stream is converted into text and
processed using a pretrained BERT model.

The `[CLS]` representation is used as the sentence-level feature vector.

### Multimodal Fusion

Visual, audio, and textual feature vectors are integrated using a
Multi-modal Multi-utterance Bi-modal Attention (MMMU-BA) framework.

The fused representation is used for:

1. Deepfake detection
2. Source identity identification

## Dataset

The project uses the **FakeAVCeleb** dataset, a multimodal deepfake
dataset containing both manipulated video and synthesized audio.

Dataset repository:

https://github.com/DASH-Lab/FakeAVCeleb

## Technologies

- Python
- PyTorch
- Wav2Vec 2.0
- BERT
- MTCNN
- I3D
- Deep Learning
- Multimodal Learning
- Attention Mechanisms

## Project Structure

```text
.
├── src/
│   ├── audio/
│   ├── video/
│   ├── text/
│   ├── multimodal/
│   └── utils/
├── models/
├── notebooks/
├── figures/
├── requirements.txt
└── README.md
```
