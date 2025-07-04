# 🛡️ Large Language Models for Cybersecurity (Bachelor Thesis)

> **Bachelor Thesis – July 2025**  
> Mohamed Elquesni · German University in Cairo (GUC)

---

## 📌 Overview

This project investigates the application of **decoder-based Large Language Models (LLMs)** for solving key cybersecurity challenges. While encoder models like BERT have dominated past research, this thesis focuses on instruction-tuned decoder models (e.g., Mistral, LLaMA, Gemma, DeepSeek) and shows their capability in realistic SOC-like tasks.

Experiments were conducted using **Google Colab Pro** with 4-bit quantized models and **QLoRA fine-tuning** via the [Unsloth](https://github.com/unslothai/unsloth) framework.

---

## 🔐 Implemented Tasks

| Task                            | Model Used                           | Dataset / Source                           | Output Type         |
|---------------------------------|--------------------------------------|--------------------------------------------|---------------------|
| **Phishing Email Detection**    | Mistral 7B Instruct (Unsloth)        | 5 curated phishing datasets                | Structured JSON     |
| **Threat Intelligence Extraction** | LLaMA 3.1 Instruct                  | CTI-HAL Dataset                             | MITRE TTP JSON      |
| **Log Anomaly Detection**       | Gemma 1.1 Instruct (Unsloth)         | KDDCup'99                                   | Binary Class Label  |
| **Threat Hunting Query Generation** | DeepSeek-Coder 6.7B Instruct      | Custom SPL instruction-template dataset     | SPL Queries         |

---

## 📊 Results Snapshot

> 📌 Full evaluations are available in the notebook per task directory.

| Task                      | Accuracy / Effectiveness            | Notes                                   |
|--------------------------|-------------------------------------|-----------------------------------------|
| Phishing Detection       | 92–97% accuracy                     | JSON preserved in ~98% of completions   |
| CTI Extraction           | 87% micro-F1                        | High TTP alignment                      |
| Log Anomaly Detection    | 96.2% binary classification         | Decoder outperformed encoder baseline   |
| SPL Query Generation     | ~90% exact template match rate      | Works well with few-shot formatting     |

---

## 💻 Directory Structure

```
📁 phishing/               → Detection experiments across datasets  
📁 cti/                    → MITRE TTP extraction from CTI reports  
📁 logs/                   → Log anomaly detection using KDD  
📁 spl_templates/          → Query generation using SPL instructions  
📁 fine_tuning/            → QLoRA notebooks using Unsloth  
📁 evaluation/             → Accuracy, F1, and output structure checks  
```

---

## 🧪 Tools Used

- 🧠 **LLMs**: Mistral 7B, LLaMA 3.1, Gemma 1.1, DeepSeek-Coder  
- 🔧 **Fine-tuning**: QLoRA 4-bit using Unsloth  
- ☁️ **Platform**: Google Colab Pro + A100  
- 🧰 **Libraries**: Hugging Face Transformers, Datasets, PEFT, Accelerate

---

## 📸 Screenshots & Examples

> 📍 Add visuals of prompt structure, generated JSON, CTI extraction, and SPL generation here:

```
📷 [screenshot-placeholder-1.png]
📷 [screenshot-placeholder-2.png]
📷 [screenshot-placeholder-3.png]
```

---

## 📘 Thesis Abstract

This thesis explores the effectiveness of decoder-based LLMs for key cybersecurity tasks. Through fine-tuning and structured prompt design, these models successfully handle phishing email classification, CTI extraction using MITRE ATT&CK alignment, KDD-based anomaly detection, and SPL query generation. The project highlights the potential of decoder architectures for SOC workflows and supports their use in privacy-preserving, local inference setups.

---

## 🧠 Author

**Mohamed Elquesni**  
German University in Cairo (GUC)  
[LinkedIn](https://www.linkedin.com/in/mohamedelquesni) · [Email](mailto:mohamedelquesni@outlook.com)  
Cairo, Egypt  

---

## 🏁 Acknowledgments

Thanks to my advisor, the Unsloth team, and the cybersecurity ML research community.

---
