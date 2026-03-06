CT-to-MRI Image Translation using Deep Learning
Overview

This project focuses on translating medical images from Computed Tomography (CT) to Magnetic Resonance Imaging (MRI) using deep learning techniques from Computer Vision and Deep Learning.

Medical imaging modalities such as CT and MRI provide complementary diagnostic information. However, MRI scans can be expensive, time-consuming, and less accessible in some clinical settings.

The goal of this project is to develop a deep learning model capable of generating synthetic MRI images from CT scans, which may help support medical analysis when MRI is unavailable.

Project Objectives

Build a model to translate CT scans into MRI images

Learn cross-modality relationships between CT and MRI

Evaluate generated MRI images using image similarity metrics

Explore the application of image-to-image translation models

Dataset

The dataset used in this project contains:

18 patients

Each patient includes:

CT scans

MRI T1 scans

MRI T2 scans

These images correspond to the same patient, allowing supervised training between CT and MRI modalities.

Medical images are commonly stored in formats such as:

DICOM

NIfTI

Methodology

The project follows a typical medical imaging pipeline:

1. Data Preprocessing

Load medical images

Slice extraction from 3D volumes

Image normalization

Alignment between CT and MRI images

Libraries used for handling medical images include:

pydicom

NiBabel

SimpleITK

2. Model Architecture

The project uses image-to-image translation models such as:

Pix2Pix

CycleGAN

These models are widely used for cross-modality medical image translation.

3. Training

The models are trained using deep learning frameworks such as:

PyTorch
or

TensorFlow

Training includes:

CT images as input

MRI images as target output

Adversarial and reconstruction loss functions

Evaluation Metrics

Generated MRI images are evaluated using common image quality metrics:

Structural Similarity Index

Peak Signal-to-Noise Ratio

Mean Squared Error (MSE)

These metrics measure similarity between generated MRI images and real MRI scans.

Technologies Used

Python

NumPy

OpenCV

PyTorch / TensorFlow

CT-to-MRI-Translation
│
├── data
│   ├── CT
│   ├── MRI_T1
│   └── MRI_T2
│
├── preprocessing
│   └── data_preprocessing.py
│
├── models
│   ├── pix2pix_model.py
│   └── cyclegan_model.py
│
├── training
│   └── train.py
│
├── evaluation
│   └── metrics.py
│
├── results
│   └── generated_images
│
└── README.md


Future Work

Increase dataset size

Improve image registration

Train on 3D medical volumes

Apply models for clinical decision support

Disclaimer

This project is intended for research and educational purposes only.
The generated MRI images are not intended for clinical diagnosis without medical validation.
Medical imaging libraries

GPU acceleration
