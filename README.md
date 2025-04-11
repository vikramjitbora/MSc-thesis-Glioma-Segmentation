# Automated Glioma Segmentation on Post-Treatment MRI Scans using Deep Neural Networks

**Author:** Vikramjit Bora  
**Degree:** M.Sc. in Artificial Intelligence and Machine Learning  
**University:** University of Birmingham  

---

## Overview

This dissertation addresses the critical challenge of segmenting gliomas in post-treatment MRI scans—a task crucial for improving clinical outcomes in brain tumor patients. By developing a novel deep learning architecture that combines residual connections and spatial attention mechanisms within a 3D U-Net framework, the research significantly enhances the differentiation between residual tumor tissue and treatment-related changes.


## Abstract

Gliomas are among the most aggressive brain tumors, and their post-treatment management is complicated by anatomical changes and treatment artifacts in MRI scans. This work introduces a **Residual 3D U-Net with Attention** that leverages deep neural networks to improve segmentation accuracy. The model is designed to capture both fine structural details and high-level contextual information, which is crucial for distinguishing between residual tumor tissue and treatment effects. The research demonstrates significant improvements in segmentation performance, validated by metrics such as the Dice Coefficient and lesion-wise sensitivity.

---

## Motivation and Objectives

- **Clinical Relevance:** Improve the accuracy of glioma segmentation in post-treatment MRIs, aiding in more effective patient management.
- **Technical Challenge:** Address the difficulties introduced by resection cavities and treatment-induced artifacts.
- **Research Objectives:**
  - Enhance segmentation accuracy through a novel architecture.
  - Tackle class imbalance with a combined loss function (focal loss + cross-entropy loss).
  - Provide robust quantitative and qualitative evaluation of the proposed method.

---

## Technical Contributions

- **Architecture Innovation:**  
  Combines residual connections with a spatial attention mechanism in a 3D U-Net framework to enhance feature learning.
- **Loss Function Design:**  
  Utilizes a customized loss function that integrates focal loss and cross-entropy loss, effectively addressing the imbalance in tumor versus background regions.
- **Evaluation Metrics:**  
  Employs lesion-wise Dice Coefficient and sensitivity metrics to rigorously assess segmentation performance.
- **Comparative Study:**  
  Demonstrates the advantages of the proposed model over standard 3D U-Net variants in terms of segmentation accuracy and robustness.

---

## Methodology

1. **Model Architecture:**
   - **Encoder:** Extracts multi-scale features using residual blocks and max-pooling.
   - **Decoder:** Utilizes transpose convolutions for upsampling and integrates encoder features via skip connections.
   - **Attention Mechanism:** Applies spatial attention to focus on the most relevant regions for segmentation.
2. **Loss Function:**  
   A combined loss function balances focal loss and cross-entropy loss to improve training stability and performance.
3. **Implementation:**  
   Detailed experimentation with learning rate schedulers and regularization techniques ensured optimal training of the network on the BraTS 2024 dataset.

---

## Experiments and Results

- **Dataset:**  
  Utilizes a subset of the 2024 BraTS dataset for post-treatment glioma segmentation.
- **Evaluation:**  
  The proposed model consistently achieves higher Dice scores (up to ~0.87 for whole tumor segmentation) and improved sensitivity, outperforming baseline models.
- **Visual Analysis:**  
  Qualitative results show close alignment between predicted segmentation and ground truth, particularly in delineating complex tumor boundaries and resection cavities.


## Contact

For further details or collaboration inquiries, please feel free to contact me:

- **Email:** vikramjit.bora@gmail.com
- **LinkedIn:** https://www.linkedin.com/in/vikramjitbora/

---

*This repository is a demonstration of my master's dissertation work aimed at advancing medical image segmentation through deep learning techniques.*
