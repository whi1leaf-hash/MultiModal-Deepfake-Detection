# Multimodal Deepfake Detection and Source Identification

Research project exploring the use of audio, video, and text features for deepfake detection and source identification. This repository collects the project notebooks and final presentation. It is a research archive; the notebooks are exploratory and do not form a complete, verified end-to-end training pipeline.

## Project at a glance

The project explores these components, as described in the paper and final presentation:

- **Audio:** Wav2Vec 2.0 feature extraction and speech-to-text experiments.
- **Text:** sentence embeddings using BERT.
- **Video:** MTCNN face detection example, plus presentation material on key-frame selection, visual features, and Xception-based frame voting.
- **Multimodal:** the research design discusses combining modalities with MMMU-BA for deepfake detection and source identification.

The provided code includes exploratory notebooks for audio, text, and an MTCNN example. It does not include an integrated Xception/SAD/MMMU-BA implementation or a complete reproducible training and evaluation pipeline. The presentation reports gradient explosion and further model optimization as outstanding work.

## Repository contents

```text
.
├── README.md
├── UPLOAD_TO_GITHUB_WINDOWS.md
├── requirements.txt
├── data/README.md
├── docs/Final_Presentation.pptx
└── notebooks/
    ├── audio/
    ├── text/
    └── vision/
```

## Getting started

1. Use Python 3.10 or later and install the packages in `requirements.txt`.
2. Open the notebooks with Jupyter Lab or Jupyter Notebook.
3. Where a notebook needs FakeAVCeleb, download the dataset according to its project terms, then set `FAKEAVCELEB_DIR` to the local dataset directory. See [`data/README.md`](data/README.md).
4. Pretrained Hugging Face model weights may be downloaded on first use. GPU use depends on installing a PyTorch build compatible with your CUDA setup.

The notebooks have had saved outputs and machine-specific absolute paths removed. They have not been run end-to-end in this repository, and some cells may need adjustment for current library versions and dataset layouts.

## Dataset and privacy

The FakeAVCeleb dataset is not included. Do not commit dataset videos, audio, transcripts, generated features, model weights, or personal data. The original upload also contained a separate Stop Asian Hate CSV, a generated label array, a local training manifest with transcripts and workstation paths, and a sample face image; these are excluded from this project archive.

## Publication

Yahan Zheng, Xu Zhou, Cheng Chen, and Jingwen Hu. “Multi-Modal Solution: Deepfake Detection and the Source Identification.” Proceedings of the 3rd International Conference on Public Management and Big Data Analysis (PMBDA 2023), published 2024. [https://doi.org/10.4108/eai.15-12-2023.2345299](https://doi.org/10.4108/eai.15-12-2023.2345299)

## Acknowledgment and licensing

This repository contains work from a collaborative research project. Preserve the original authorship and cite the publication when reusing the research. The repository does not add a license; confirm that all contributors agree on a license before granting reuse rights. Third-party models, datasets, and libraries remain subject to their own terms.
