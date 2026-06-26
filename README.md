# DentAI — Dental Caries Detection via Transfer Learning

> **Published in Springer · DOI: 10.1007/s12652-024-04795-x · 150+ Google Scholar Citations**

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square&logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Transfer%20Learning-FF6F00?style=flat-square&logo=tensorflow)
![Published](https://img.shields.io/badge/Published-Springer-red?style=flat-square)
![Citations](https://img.shields.io/badge/Citations-150%2B-brightgreen?style=flat-square)
![Domain](https://img.shields.io/badge/Domain-Medical%20AI-purple?style=flat-square)

---

## Overview

Dental caries (tooth decay) is one of the most prevalent chronic diseases globally — yet early detection relies heavily on subjective clinical judgment and X-ray interpretation, which varies significantly across practitioners.

This project implements and compares **5 state-of-the-art CNN architectures** using transfer learning to automatically detect dental caries from dental images, with gradient-based class activation mapping (Grad-CAM) for interpretability — a critical requirement in clinical AI systems.

**Published in Springer:** [AI-enabled dental caries detection using transfer learning and gradient-based class activation mapping](https://link.springer.com/article/10.1007/s12652-024-04795-x)

---

## Models Compared

| Model | Architecture Type | Notable Strength |
|---|---|---|
| **EfficientNetV2B3** | Compound scaling | Best accuracy/compute tradeoff |
| **InceptionResNetV2** | Inception + ResNet hybrid | Deep feature extraction |
| **ResNet50** | Residual connections | Strong baseline, proven depth |
| **VGG19** | Deep sequential CNN | Interpretable feature maps |
| **Xception** | Depthwise separable convs | Efficient spatial feature learning |

Each model is implemented in a dedicated notebook for clean comparison:
- `Dentistry_efficientNetV2B3.ipynb`
- `Dentistry_InceptionResnetV2.ipynb`
- `Dentistry_Resnet50.ipynb`
- `Dentistry_VGG19.ipynb`
- `Dentistry_Xception.ipynb`

---

## Key Technical Contributions

**Transfer Learning Strategy:**
ImageNet-pretrained weights provide a strong visual feature foundation. The top classification layers are replaced and fine-tuned on dental imagery — enabling high accuracy even with limited medical imaging data, where large labeled datasets are expensive to obtain.

**Grad-CAM Visualization:**
Gradient-based Class Activation Mapping produces heatmaps highlighting *which regions of the dental image* drove the model's decision. This is not optional in medical AI — it's what makes the model clinically trustworthy and interpretable to practitioners.

```
Dental X-ray → Pretrained CNN → Fine-tuned classifier
                                        ↓
                              Grad-CAM heatmap
                              (highlights carious regions)
                                        ↓
                              Detection + confidence score
```

---

## Publication

**"AI-enabled dental caries detection using transfer learning and gradient-based class activation mapping"**

- **Journal:** Springer (Journal of Ambient Intelligence and Humanized Computing)
- **DOI:** [10.1007/s12652-024-04795-x](https://link.springer.com/article/10.1007/s12652-024-04795-x)
- **Citations:** 150+ (Google Scholar)

This work contributes to the growing body of research on AI-assisted diagnostics — specifically addressing the clinical need for explainable, accurate, and accessible dental screening tools.

---

## Quick Start

```bash
git clone https://github.com/Drashti0913/Teeth-Caries-Detection-using-Transfer-Learning.git
cd Teeth-Caries-Detection-using-Transfer-Learning

pip install -r requirements.txt

# Run any model notebook
jupyter notebook Dentistry_efficientNetV2B3.ipynb
```

---

## Clinical Context

**Why this matters:**
- Caries affects ~2.5 billion people globally (WHO)
- Early detection dramatically reduces treatment complexity and cost
- Rural and underserved areas lack specialist dental diagnosticians
- An AI-assisted screening tool could enable point-of-care detection with a smartphone camera

**Why Grad-CAM is essential:**
A black-box classifier is insufficient for clinical adoption. Grad-CAM provides spatial justification for predictions — allowing clinicians to verify the model is attending to the correct anatomical regions rather than spurious correlations in the background.

---

## Results

> Full accuracy, precision, recall, and F1 metrics for each of the 5 architectures are available in the published paper and individual notebooks.
> Add your best model result here: Best model: VGG-19 · Accuracy: 96.58% · 

---

## License

MIT
