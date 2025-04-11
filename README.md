# Automated Glioma Segmentation on Post-Treatment MRI Scans using Deep Neural Networks

**Author:** Vikramjit Bora
**Degree:** M.Sc. in Artificial Intelligence and Machine Learning, University of Birmingham 


---

## Abstract

This research tackles the critical challenge of segmenting gliomas in post-treatment Magnetic Resonance Imaging (MRI) scans, a vital task for managing brain tumor patients. Gliomas, especially aggressive forms like glioblastomas, require accurate monitoring after treatment. However, post-treatment MRIs are complex due to surgical changes (resection cavities) and treatment-induced effects, making it hard to distinguish remaining tumor tissue from these changes. This project introduces a novel deep learning model, a **Residual 3D U-Net with an Attention mechanism**, specifically designed to improve segmentation accuracy in these challenging post-treatment conditions. By combining residual connections for deeper feature learning and spatial attention to focus on relevant areas, the model enhances the reliability of identifying residual tumor versus treatment effects, potentially leading to better clinical decision-making and patient outcomes.

## Motivation

Accurate segmentation of post-treatment MRIs is crucial for effective glioma patient management. Distinguishing residual tumor from treatment effects (like inflammation or resection cavities) informs critical decisions about further treatment (e.g., additional surgery, radiation). Manual segmentation is time-consuming and prone to variability. Automated, reliable methods can provide consistent results, aiding clinicians in making informed decisions and potentially improving patient quality of life.

## Problem Addressed

* **Complexity of Post-Treatment MRIs:** Scans taken after surgery, radiation, or chemotherapy often contain resection cavities, inflammation, and other artifacts that obscure tumor boundaries.
* **Difficulty in Differentiation:** Standard algorithms struggle to reliably distinguish residual/recurrent tumor tissue from non-cancerous treatment-related changes.
* **Performance Gap:** Many existing segmentation models are trained on pre-treatment scans and perform poorly on the unique characteristics of post-treatment images.

## Proposed Solution: Residual 3D U-Net with Attention

This project proposes and evaluates a deep neural network architecture tailored for post-treatment glioma segmentation:

* **Backbone:** Based on the proven U-Net architecture for medical image segmentation.
* **3D Convolutions:** Processes volumetric MRI data directly, preserving spatial context unlike 2D slice-by-slice methods.
* **Residual Connections:** Inspired by ResNet, these allow the network to learn deeper, more complex features by facilitating gradient flow during training, improving robustness.
* **Attention Mechanism:** Enables the model to focus selectively on the most relevant image regions (features) for segmentation, particularly useful for identifying small or subtle tumor areas amidst complex post-treatment changes.

## Key Contributions

* Developed a novel **Residual 3D U-Net with Attention** architecture specifically for segmenting gliomas in *post-treatment* MRI scans.
* Improved segmentation accuracy by effectively combining residual learning (for depth) and attention mechanisms (for focus).
* Addressed class imbalance inherent in medical datasets (e.g., small tumor regions vs. background) using a combined Focal Loss and Cross-Entropy loss function for more stable and effective training.
* Provided a comparative analysis demonstrating the superiority of the proposed model against baseline 3D U-Net, 3D U-Net with Attention, and Residual 3D U-Net architectures on key metrics like the Dice coefficient.

## Methodology & Tech Stack

* **Core Technique:** Deep Learning, 3D Convolutional Neural Networks (CNNs) based architectures.
* **Model:** Residual 3D U-Net with Attention 
* **Frameworks/Libraries:** Pytorch
* **Data:** Subset of the BraTS 2024 challenge dataset, focusing on post-treatment multi-parametric MRI scans (T1, T1-Gd, T2, FLAIR sequences)
* **Loss Function:** Combined Focal Loss and Cross-Entropy Loss 
* **Evaluation Metrics:** Lesion-wise Dice Coefficient, Sensitivity 

## Results Highlights

* The proposed **Residual 3D U-Net with Attention** model achieved the highest performance among the evaluated architectures.
* **Quantitative:** Achieved a Dice coefficient of 0.87 for whole tumor segmentation and 0.63 for resection cavity segmentation on the test subset, demonstrating significant improvement over baseline models.
* **Qualitative:** Visual analysis showed the model accurately segmented tumors and resection cavities in many cases, though challenges remain with highly irregular shapes or fine details.

## Code Repository

The complete code, including data loading, preprocessing, model implementation, training, and evaluation, is available in the `segmentation.ipynb` Jupyter Notebook within the project's GitLab repository:

[**View Code on GitLab**] - https://git.cs.bham.ac.uk/projects-2023-24/vxb330


## How to Run

Instructions for setting up the environment and running the code can be found within the `segmentation.ipynb` notebook in the repository. Key steps involve data loading, preprocessing, model definition, and executing the training/evaluation cells.

## Keywords

Glioma Segmentation, Brain Tumor, Post-Treatment MRI, Deep Learning, Medical Image Segmentation, 3D U-Net, Residual Networks (ResNet), Attention Mechanism, Convolutional Neural Networks (CNN), Artificial Intelligence, Machine Learning, BraTS Challenge
