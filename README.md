<div align="center">

<img src="https://media.giphy.com/media/MDJ9Ibxx5ASScEfyfh/giphy.gif" width="80px">

# 𝖯𝖾𝖽𝗂𝖺𝖵𝗂𝗌𝗂𝗈𝗇

### *Advanced Pediatric Skin Analysis System*

> A multi-stage deep learning pipeline for skin condition classification, interactive AI-assisted diagnosis, and personalized treatment recommendations. Trained on HAM10000 + ACNE04 with EfficientNet-B3 achieving 82.5% validation accuracy.

[![Python](https://img.shields.io/badge/Python-3.10+-FFB7B2?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-FFDAC1?style=flat-square&logo=pytorch&logoColor=white)](https://pytorch.org/)
[![Accuracy](https://img.shields.io/badge/Validation_Accuracy-82.5%25-B5EAD7?style=flat-square)](https://github.com/vnnviv/PediaVision)
[![Architecture](https://img.shields.io/badge/Architecture-EfficientNet--B3-C7CEEA?style=flat-square)](https://github.com/vnnviv/PediaVision)
[![Dataset](https://img.shields.io/badge/Training_Samples-8%2C012-E2F0CB?style=flat-square)](https://github.com/vnnviv/PediaVision)

⸜(｡˃ ᵕ ˂ )⸝♡

</div>

---

### ⋆˚✿˖° Overview

> **PediaVision** is a complete four-stage AI pipeline for skin condition analysis developed for integration into the **[SpotCheck iOS Application](https://github.com/vnnviv/SpotCheck)**. The system goes beyond simple image classification, it combines CNN-based visual analysis with AI-assisted clarification questions and evidence-based treatment recommendations.

* ʚɞ **Demographic Fairness:** Specifically designed with demographic fairness in mind, addressing known gaps in dermatological AI systems that underperform on darker skin tones and East/Southeast Asian skin types.

---

### ᧔ෆ᧓ System Architecture — Four Stages

* ʚɞ **Stage 1: CNN Analysis**
  * ✦ EfficientNet-B3 classifies uploaded image ┈➤ Initial diagnosis + predictive scores
* ʚɞ **Stage 2: AI Clarification (Fine-tuned LLaMA)**
  * ✦ Asks targeted questions ┈➤ Age, symptom duration, prior treatments, skin tone
* ʚɞ **Stage 3: Refined Diagnosis**
  * ✦ Combines visual features + questionnaire responses ┈➤ Updated predictive score
* ʚɞ **Stage 4: Treatment Recommendations**
  * ✦ Personalized product recommendations ┈➤ Curated from structured Sephora/Amazon treatment database

---

###  Model Performance & Data

#### ˚˖𓍢ִ໋❀ Metrics

* ʚɞ **Architecture:** EfficientNet-B3
* ʚɞ **Training Samples:** 8,012
* ʚɞ **Validation Samples:** 2,003
* ʚɞ **Validation Accuracy:** **82.52%**
* ʚɞ **Input Resolution:** 224 × 224 px
* ʚɞ **Output Classes:** 7

<br />

#### ˚˖𓍢ִ໋❀ Classification Classes

| Class | Description |
| :--- | :--- |
| **Actinic Keratoses** | Pre-cancerous rough skin patches |
| **Basal Cell Carcinoma** | Most common form of skin cancer |
| **Benign Keratosis** | Non-cancerous skin growths |
| **Dermatofibroma** | Benign fibrous skin nodules |
| **Melanocytic Nevi** | Common moles |
| **Melanoma** | Malignant skin cancer |
| **Vascular Lesions** | Blood vessel abnormalities |

<br />

#### ˚˖𓍢ִ໋❀ Datasets

* ʚɞ **HAM10000:** Human Against Machine — skin lesion classification (~10,000 images)
* ʚɞ **ACNE04:** Acne severity classification, Grade 1–4 (~4,000 images)

---

###  Tech Stack

* ʚɞ **Core ML:** `torch` · `torchvision` · `efficientnet_pytorch` · `transformers` · `peft` (LLaMA fine-tuning via PEFT/LoRA)
* ʚɞ **Data & Evaluation:** `pandas` · `numpy` · `scikit-learn` · `opencv-python` · `PIL` · `matplotlib` · `seaborn`
* ʚɞ **Deployment & UI:** `CoreML` (via `coremltools`) · `gradio` (interactive demo interface)

