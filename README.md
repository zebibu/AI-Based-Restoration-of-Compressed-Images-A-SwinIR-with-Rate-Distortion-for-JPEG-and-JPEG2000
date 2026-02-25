# AI-Based-Restoration-of-Compressed-Images-A-SwinIR-with-Rate-Distortion-for-JPEG-and-JPEG2000

# AI-Based Restoration of Compressed Images using SwinIR  
### Rate–Distortion Analysis for JPEG and JPEG2000

---

## 📌 Overview

This project investigates **AI-based restoration of compressed images** using the **SwinIR (Swin Transformer for Image Restoration)** framework.

The study evaluates the effectiveness of transformer-based restoration for:

- 📷 JPEG compression artifacts (DCT-based)
- 📷 JPEG2000 compression artifacts (Wavelet-based)

Additionally, a **JPEG2000-adapted architecture** is implemented to improve restoration performance for wavelet distortions.

---

## 🎯 Objectives

This project addresses three main tasks:

### (a) JPEG Restoration
- Apply pretrained **SwinIR JPEG artifact removal model**
- Test across multiple compression factors
- Evaluate performance using:
  - PSNR
  - SSIM
  - Rate–Distortion (R–D) Curves

### (b) JPEG2000 Evaluation
- Apply the **same JPEG-trained SwinIR model**
- Analyze generalization to JPEG2000 compressed images
- Compare performance trends

### (c) JPEG2000-Adaptive Architecture
- Design a lightweight **JP2-specific PreNet**
- Fine-tune on JPEG2000 compressed images
- Compare against baseline SwinIR

---

## 🧠 Key Findings

- SwinIR significantly improves JPEG compressed images.
- Performance degrades when applying JPEG-trained SwinIR to JPEG2000 due to artifact mismatch.
- A lightweight JP2-adapted architecture improves restoration for JPEG2000.
- Artifact-specific modeling is crucial for compression restoration tasks.

---

## 🏗 Architecture

### 1️⃣ SwinIR (Baseline Engine)
- Transformer-based image restoration
- Trained for JPEG compression artifact removal
- Window-based self-attention mechanism

### 2️⃣ JP2-Adapted PreNet
- Multi-scale dilated convolution module
- Residual learning structure
- Designed to handle wavelet-based artifacts
- Trained separately without backpropagating through SwinIR

---

## 📊 Evaluation Metrics

- **PSNR (Peak Signal-to-Noise Ratio)**
- **SSIM (Structural Similarity Index)**
- **Rate–Distortion Curves**
  - File Size (KB) vs PSNR (dB)

---

## 🛠 Technologies Used

- Python
- PyTorch
- OpenCV
- SwinIR (Transformer architecture)
- OpenJPEG (via Glymur)
- NumPy
- Matplotlib
- scikit-image

---

## 🚀 How to Run

### 1️⃣ Install dependencies

```bash
pip install torch torchvision scikit-image glymur opencv-python
