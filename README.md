



# Master's Thesis

## AI-based Reconstruction and Denoising for Robust Structured Illumination Microscopy at Low Signal-to-Noise Ratios

# Abstract
Fluorescence microscopy is a powerful imaging technique that enables the visualization of biological specimens at cellular and subcellular level with a resolution
limit of 200-300 nm. The development of structured illumination microscopy (SIM)
has further enhanced resolution by exploiting the interference of light patterns to
achieve SIM reconstructions with two times the resolution. However, imaging biological specimens under microscopy faces fundamental challenges, such as imaging
speed, light exposure, and spatial resolution. Specifically, imaging biological specimens often requires rapid acquisition with high temporal resolution and low light
exposure to reduce photo-bleaching and photo-toxicity. These requirements typically lead to low-SNR imaging, which results in poor SIM reconstruction with a
high level of reconstruction artifacts. In contrast, high-SNR imaging produces superior quality at the cost of slower speeds and increased light exposure, which can
potentially jeopardize the sensitive specimens.


In this work, we explore the feasibility of recovering spatial and temporal resolution
hidden in low-SNR images by leveraging state-of-the-art deep learning techniques.
Our approach is centered on a novel direct SIM reconstruction methodology using
Projection Upsampling Network (PU-Net), which replaces the Deep Fourier Channel
Attention Network (DFCAN) module in the current RDL-SIM training pipeline,
which consists of predicting SIM reconstruction images with a pre-trained network
(DFCAN) and convolving this image with a prior knowledge-based sinusoidal pattern
to simulate moir´e fringes for training the final denoising module, as proposed by Qiao
et al., 2022.



[![Read Thesis](https://img.shields.io/badge/PDF-Read%20Thesis-red?style=for-the-badge&logo=adobeacrobatreader)](AI-based-Reconstruction-and-Denoising-for-Robust-Structured-Illumination-Microscopy-at-Low-Signal-to-Noise-Ratios.pdf)
