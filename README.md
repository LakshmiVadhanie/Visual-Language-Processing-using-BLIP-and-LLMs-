# Vision-Language Understanding with BLIP, VLP, and Mistral7B

This project implements a vision-language understanding system that integrates **BLIP**, **VLP**, and **Mistral7B** models. The system is trained on the COCO dataset for general-purpose image captioning and fine-tuned on MIMIC-CXR for healthcare-specific tasks. It supports caption generation and image-based question answering.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
  - [Training](#training)
  - [Evaluation](#evaluation)
  - [Inference](#inference)
- [Results](#results)
- [Future Work](#future-work)


---

## Introduction

Vision-language understanding is a crucial aspect of AI systems that bridge visual and textual data. This project leverages:
- **BLIP (Bootstrapped Language-Image Pretraining):** A model for efficient vision-language representation learning.
- **VLP (Vision-Language Pretraining):** Advanced model for multimodal tasks.
- **Mistral7B:** A powerful large language model for natural language understanding.

**Goals:**
1. Train BLIP and VLP on COCO for general-purpose captioning.
2. Fine-tune models on MIMIC-CXR for healthcare-related tasks.
3. Enable multimodal reasoning by integrating these models with Mistral7B.

---

## Dataset

### COCO Dataset
- General-purpose dataset for image captioning.
- Download: [COCO Dataset](https://cocodataset.org)

### MIMIC-CXR Dataset
- Chest X-ray dataset for domain-specific applications.
- Access: [MIMIC-CXR](https://physionet.org/content/mimic-cxr/)

**Dataset Organization:**
/content/coco/coco2017/ ├── annotations/ │ ├── captions_train2017.json │ ├── captions_val2017.json └── train2017/ └── <image files> /content/mimic-cxr/ └── <image and annotation files>

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
Install dependencies:

## 2. Install Dependencies

To install the required dependencies for the project, run the following command:

```bash
pip install -r requirements.txt



## 3. Authenticate with Hugging Face Hub 

   ```bash
  from huggingface_hub import login
  login(token="your_huggingface_token")


##4. Usage
Training
Fine-tuning on COCO
##5. Run the training script:

   ```bash
  python train_blip.py --dataset coco --epochs 5 --batch_size 16

##6. Fine-tuning on MIMIC-CXR
Update the dataset paths in the script and run:

   ```bash
  python train_blip.py --dataset mimic --epochs 5 --batch_size 16

##7. Evaluation
Evaluate on a validation dataset:

   ```bash
  python evaluate.py --model blip --dataset coco


##8. Generate Captions

   ```bash
  from inference import generate_caption
  caption = generate_caption("path/to/image.jpg")
  print("Generated Caption:", caption)

##9. Question Answering


  ```bash
  from inference import answer_question

  answer = answer_question("path/to/image.jpg", "What is in the image?")
  print("Answer:", answer)
