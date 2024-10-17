# Health Analytics Project – Milestone 01

## Group Members
- Ran Arino
- Zubeka Dane Dang

## Brain Tumor Image Analysis Project Proposal

### 1. Problem to be Solved/Analyzed

The primary problem we will address is the segmentation of brain tumors in multimodal magnetic resonance imaging (MRI) scans. Specifically, we will focus on segmenting three tumor sub-regions:

1. GD-enhancing tumor (ET)
2. Peritumoral edema (ED)
3. Necrotic and non-enhancing tumor core (NCR/NET)

Accurate segmentation among these regions is crucial for diagnosis, treatment planning, and monitoring of brain tumors. By developing an automated segmentation method, it is expected to assist medical professionals in more efficiently and accurately analyzing brain tumor MRI scans.

### 2. Data and Data Sources

We will utilize the Brain Tumor Segmentation (BraTS) 2020 dataset, which includes:

- Multimodal MRI scans in NIfTI format (.nii.gz):
  - Native T1-weighted (T1)
  - Post-contrast T1-weighted (T1Gd)
  - T2-weighted (T2)
  - T2 Fluid Attenuated Inversion Recovery (T2-FLAIR)
- Manual segmentation labels for tumor sub-regions
- Clinical data on overall survival
- Progression status evaluations
- Uncertainty estimations for predicted tumor sub-regions

The dataset is pre-processed, co-registered to the same anatomical template, interpolated to 1 mm³ resolution, and skull-stripped. All slices have been converted to HDF5 format for efficient memory usage.

Considering that the dataset has more than 57k images and close to 7GB, we are likely to reduce the number of training datasets for more efficient and faster model training.

Data source: BraTS 2020 challenge, comprising scans from multiple institutions (n=19).

[BraTS 2020 Dataset on Kaggle](https://www.kaggle.com/datasets/awsaf49/brats20-dataset-training-validation)

### 3. Business/Challenge Questions

Our project will address the following key questions:

1. How accurately can we segment the three tumor sub-regions (ET, ED, NCR/NET) using deep learning techniques?
2. What is the best performed model by comparing with various state-of-the-art models and benchmarks?

### 4. Solution Strategy

Our approach to solving this challenge will involve the following steps:

#### 4.1 Research for State-of-the-art Segmentation Model
- Focusing on literature review about the MRI segmentation from 2020
- Identify the state-of-the-art models to compare them with the benchmark models

#### 4.2 Data Preprocessing and Exploration
- Analyze the distribution of tumor types and sizes in the dataset
- Visualize sample MRI scans and corresponding segmentation masks
- Implement data augmentation techniques to increase dataset diversity (optional)

#### 4.3 Model Development
- Design and implement a GAN model for multimodal MRI segmentation and compare with the performance of other model, such as U-Net
- Incorporate attention mechanisms to focus on relevant features in different MRI modalities
- Implement a multi-task learning approach to simultaneously segment tumor sub-regions and estimate segmentation uncertainty

#### 4.4 Training and Validation
- Use k-fold cross-validation to ensure robust model performance and prevent bias
- Implement early stopping or learning rate scheduling to optimize training
- Use appropriate loss functions for segmentation tasks

#### 4.5 Performance Evaluation
- Evaluate model performance using standard metrics (Dice score, Hausdorff distance)
- Compare the model's performance that we used against state-of-the-art methods from previous BraTS challenges

#### 4.6 Documentation and Reporting
- Prepare a comprehensive report detailing our methodology, results, and findings
- Create visualizations to effectively communicate our results to both technical and clinical audiences

By following this strategy, we aim to develop a robust and clinically relevant solution for brain tumor segmentation that can potentially improve the efficiency and accuracy of brain tumor analysis in clinical settings.