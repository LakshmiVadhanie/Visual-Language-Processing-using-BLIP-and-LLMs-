# Vision-Language Understanding Using BLIP, VLP, and Mistral7B

This project implements vision-language understanding by fine-tuning and integrating BLIP, VLP, and Mistral7B models. The system generates captions for input images and answers questions related to the images. The COCO dataset is used for pretraining and fine-tuning the models, and MIMIC-CXR is leveraged for domain-specific fine-tuning in the healthcare domain.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
  - [Training](#training)
  - [Evaluation](#evaluation)
  - [Image Captioning](#image-captioning)
  - [Question Answering](#question-answering)
- [Model Integration](#model-integration)
- [Results](#results)
- [Future Work](#future-work)
- [Contributors](#contributors)
- [License](#license)

---

## Introduction

This project integrates three state-of-the-art models:
- **BLIP (Bootstrapped Language-Image Pretraining):** For image captioning.
- **VLP (Vision-Language Pretraining):** To enhance vision-language tasks.
- **Mistral7B (LLM):** A generative language model for natural language understanding and reasoning.

### Objectives
1. Fine-tune BLIP and VLP on the COCO dataset for image captioning.
2. Fine-tune these models on the MIMIC-CXR dataset for healthcare domain-specific captions.
3. Integrate BLIP, VLP, and Mistral7B to enable caption generation and question answering.

---

## Dataset

### COCO Dataset
- **Purpose:** General-purpose image captioning.
- **Download:** [COCO Dataset](https://cocodataset.org)

### MIMIC-CXR Dataset
- **Purpose:** Domain-specific captioning for chest X-rays.
- **Access:** Follow instructions at [MIMIC-CXR](https://physionet.org/content/mimic-cxr/)

---
