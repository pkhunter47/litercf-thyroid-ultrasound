<div align="center">

# LiteRCF-Net for Thyroid Ultrasound Classification

### Lightweight region–context–frequency learning with marker-robust training

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Backbone](https://img.shields.io/badge/Backbone-MobileNetV4--Conv--Small-5C7CFA)](https://github.com/huggingface/pytorch-image-models)
[![Dataset](https://img.shields.io/badge/Primary-TN5000-2F9E44)](https://github.com/pkhunter47)

</div>

## Overview

LiteRCF-Net is a lightweight binary thyroid-ultrasound classifier designed to combine lesion appearance, peri-lesional context, and frequency information while reducing reliance on crosshair and bright-marker artifacts.

## Architecture

The notebook implements a shared MobileNetV4-Conv-Small encoder, lesion and 25% context views, a fixed four-filter Haar branch, adaptive gated fusion, calibrated classification, marker intervention, and Jensen–Shannon consistency regularization.

## Evaluation protocol

- Primary benchmark: TN5000, using official splits when available
- Deterministic grouped fallback split when official files are absent
- Folder-based thyroid dataset reserved for external evaluation
- Duplicate screening across primary and external datasets
- Untouched test evaluation, threshold calibration, ablation, and multi-seed reporting

## Quick start

Open `notebooks/litercf_colab_t4_thyroid.ipynb` in Google Colab, configure `KAGGLE_USERNAME` and `KAGGLE_KEY` as private runtime variables, and run the cells in order on a T4 GPU.

## Status and responsible use

The notebook contains the experimental pipeline but no saved outputs or credentials. Reported performance must come from a complete rerun. This research code is not approved for clinical diagnosis or patient management.

## Contact

**Protik Biswas** · [GitHub](https://github.com/pkhunter47) · [LinkedIn](https://www.linkedin.com/in/protik-biswas-83001827b/)
