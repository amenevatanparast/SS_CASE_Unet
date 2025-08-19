```markdown
# SS_CASE_UNet: An Attention-Enhanced Semi-Supervised Framework for Fetal Cerebellum Segmentation

This repository contains the resources for the paper:

**SS_CASE_UNet: An Attention-Enhanced Semi-Supervised Framework for Fetal Cerebellum Segmentation in Ultrasound Images**  
*Amene Vatanparast, Mansoor Fateh, Hoda Mashayekhi*  
Faculty of Computer Engineering, Shahrood University of Technology, Iran  

---

## 📖 Overview
Accurate segmentation of the fetal cerebellum in ultrasound images is essential for prenatal diagnostics, but it remains challenging due to image noise, anatomical complexity, and the scarcity of annotated data.  

We propose **SS_CASE_UNet**, a novel semi-supervised framework that:
- Enhances the **U-Net** architecture with **Squeeze-and-Excitation (SE)** and **Coordinate Attention (CA)** blocks.  
- Uses a **multi-stage semi-supervised training pipeline** that leverages both labeled and unlabeled data.  
- Achieves **state-of-the-art performance** while keeping model complexity practical for clinical use.  

---

## ✨ Key Contributions
- **Attention-enhanced U-Net** architecture (SE + CA blocks).  
- **Three-stage semi-supervised training strategy**:
  1. Decoder-only training  
  2. Full-network fine-tuning  
  3. Pseudo-labeling with unlabeled data  
- **Robust data augmentation pipeline** tailored for medical ultrasound images.  
- **High accuracy and robustness** despite limited annotated data.  

---

## 🧪 Results
On fetal cerebellum ultrasound segmentation, SS_CASE_UNet achieved:

| Method        | Accuracy | Precision | Recall | Jaccard | Dice |
|---------------|----------|-----------|--------|---------|------|
| U-Net         | 97.80    | 84.26     | 74.18  | 65.08   | 78.89 |
| FCRB_U-Net    | 98.66    | 92.61     | 79.95  | 76.54   | 85.74 |
| ECAU-Net      | 98.03    | 90.85     | 79.91  | 76.17   | 85.04 |
| ReU-Net       | 98.32    | 84.43     | 76.36  | 69.45   | 80.14 |
| Dual CNN      | 97.55    | 83.89     | 75.45  | 67.57   | 79.34 |
| **SS_CASE_Unet (ours)** | **99.08** | **93.49** | **82.34** | **81.76** | **87.65** |

✔ Outperforms baselines in **all metrics**  
✔ Balanced trade-off between **accuracy and complexity**  

---

## ⚙️ Implementation
- Framework: **TensorFlow 2.15**
- Backbone: **EfficientNetB0 (pretrained on ImageNet)**
- Training:  
  - Stage 1: Decoder-only (20 epochs)  
  - Stage 2: Full fine-tuning (50 epochs)  
  - Stage 3: Pseudo-label retraining (30 epochs)  
- Loss: Hybrid **Dice loss + MSE consistency loss**  
- Platform: **Google Colab (GPU)**  

---

## 📂 Repository Structure
```

├── models/            # Model architectures (U-Net, SS\_CASE\_Unet, etc.)
├── data/              # Data loading & augmentation scripts
├── training/          # Semi-supervised training pipeline
├── results/           # Evaluation results, metrics, and visualizations
├── utils/             # Helper functions (metrics, visualization, Grad-CAM, etc.)
└── README.md          # Project description

```

---

## 📊 Visual Results
![Segmentation Examples](results/segmentation_examples.png)  
*SS_CASE_Unet demonstrates superior segmentation compared to other state-of-the-art methods.*

---

## 📌 Citation
If you use this repository, please cite our paper:

```

@article{vatanparast2025sscaseunet,
title={SS\_CASE\_UNet: An Attention-Enhanced Semi-Supervised Framework for Fetal Cerebellum Segmentation in Ultrasound Images},
author={Vatanparast, Amene and Fateh, Mansoor and Mashayekhi, Hoda},
year={2025},
journal={Under Review/Submitted}
}

```

---

## 📧 Contact
For questions, please contact:  
📩 *mansoor_fateh@shahroodut.ac.ir*
    *amene.vatanparast@gmail.com*

---

## ⭐ Acknowledgments
This work was carried out at the **Faculty of Computer Engineering, Shahrood University of Technology, Iran.**  
We thank the community for open-source frameworks that made this work possible.
```

---
