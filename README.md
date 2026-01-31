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
to simulate moiré fringes for training the final denoising module, as proposed by Qiao
et al., 2022.

[![Read Thesis](https://img.shields.io/badge/PDF-Read%20Thesis-red?style=for-the-badge&logo=adobeacrobatreader)](AI-based%20Reconstruction%20and%20Denoising%20for%20Robust%20Structured%20Illumination%20Microscopy%20at%20Low%20Signal-to-Noise%20Ratios.pdf)

## Key Features

- Direct SIM reconstruction using Projection Upsampling Network (PU-Net)
- Replacement of DFCAN module in RDL-SIM pipeline
- Enhanced performance at low signal-to-noise ratios
- Reduced photo-bleaching and photo-toxicity in biological imaging

## Installation

To set up the environment for this research:

```bash
# Clone the repository
git clone https://github.com/ArghaSarker/Mather-Thesis-.git
cd Mather-Thesis-

# Create a virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install torch torchvision numpy scipy matplotlib scikit-image
pip install opencv-python pandas tqdm tensorboard
```

## Usage

Example code for SIM reconstruction using PU-Net:

```python
import torch
import numpy as np
from model import PUNet

# Load the trained model
model = PUNet()
model.load_state_dict(torch.load('punet_weights.pth'))
model.eval()

# Process low-SNR SIM images
with torch.no_grad():
    input_image = torch.from_numpy(raw_sim_data).float()
    reconstructed = model(input_image)
    
# Save the reconstructed image
reconstructed_np = reconstructed.cpu().numpy()
```

## Citation

If you use this work in your research, please cite:

```bibtex
@mastersthesis{sarker2024sim,
  title={AI-based Reconstruction and Denoising for Robust Structured Illumination Microscopy at Low Signal-to-Noise Ratios},
  author={Sarker, Argha},
  year={2024},
  school={University Name}
}
```

## References

Qiao, C., et al. (2022). Rationalized deep learning super-resolution microscopy for sustained live imaging of rapid subcellular processes. *Nature Biotechnology*.

## License

This thesis and associated materials are provided for academic purposes.
