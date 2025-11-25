<div align="center">
<h1> [AAAI'26] Uncovering and Mitigating Destructive Multi-Embedding Attacks in Deepfake Proactive Forensics </h1>
</div>

## 📢 News
* **[2025-11]** Our paper is accepted by **AAAI 2026**! 🎉
* **[2025-11]** The code are being organized and will be released shortly. Please star this repo for updates!

## ✨ Highlights
* **⚠️New Vulnerability Uncovered:** We are the first to expose **Multi-Embedding Attacks (MEA)**, demonstrating the critical fragility of existing proactive forensics methods under such attacks.
* **🛡️General Mitigation Strategy:** We propose **Adversarial Interference Simulation (AIS)**, a model-agnostic training paradigm designed to immunize models against MEA by simulating interference.
* **🚀Boosting SOTA Performance:** As a **plug-and-play solution**, AIS effectively empowers various state-of-the-art methods to resist MEA, highlighting the necessity of this new security benchmark.

## 🚀 Introduction

<div align="center">
    <img width="600" alt="image" src="figures/introduction.png?raw=true">
</div>


Illustration of the ideal proactive forensics pipeline and the threat posed by Multi-Embedding Attacks (MEA). (a) In the standard pipeline, the embedded forensic watermark is expected to withstand manipulations such as deepfake generation. (b) However, additional third-party embeddings (e.g., social media platforms or malicious actors) can overwrite and degrade the original watermark, leading to a complete failure of the proactive forensics mechanism.

## 📻 Overview

<div align="center">
    <img width="1000" alt="image" src="figures/method.png?raw=true">
</div>

<div align="center">
Overview of the proposed framework. </div>

## 🎮 Getting Started

### 1. Install Environment

To set up the experimental environment, please follow the specific requirements for each baseline model. Taking **SepMark** as an example, you can create and install the environment using the provided script:

```bash
# Navigate to the shell directory of the specific method (e.g., SepMark)
cd SepMark/fine_tuning/shell

# Run the environment setup script
bash env.sh
```

### 2. Dataset and Baseline

- We conduct experiments on the widely used high-quality [CelebA-HQ](https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html) dataset, and further performed cross-dataset evaluation on the LFW dataset.
- We select a set of representative baseline methods, including [SepMark](https://github.com/sh1newu/SepMark), [LampMark](https://github.com/wangty1/LampMark), [WaveGuard](https://github.com/Twoh11/WaveGuard), [EditGuard](https://github.com/xuanyuzhang21/EditGuard), [MBRS](https://github.com/jzyustc/MBRS), and [HiDDeN](https://github.com/ando-khachatryan/HiDDeN).

### 3. Train

To train the model using our AIS framework or to reproduce the baseline training, simply run the training script located in the shell directory:
```bash
# Ensure you are in the corresponding shell directory
bash train.sh
```
### 4. Test

To evaluate the model's performance and robustness against MEA, execute the testing script:
```bash
# Run the evaluation script
bash test.sh
```

### 5. Pretrained Model
We provide the pretrained checkpoints for all the methods mentioned in our paper. You can download them from the links below:

| Method | Checkpoint Download |
| :--- | :--- |
| **SepMark** | [Google Drive](https://drive.google.com/file/d/1g_RNS3JWbD88UmlXNBa6oWKmzvZ0qScS/view?usp=drive_link) |
| **WaveGuard** | [Google Drive](https://drive.google.com/file/d/1oia6cmhYlja8ognIdi-LQR9ONnwRowNc/view?usp=sharing) |
| **LampMark** | [Google Drive](https://drive.google.com/file/d/1m2NfcdyWCKNZS-7hxEBHE0w5QA5n7Msv/view?usp=sharing) |
| **HiDDeN** | [Google Drive](https://drive.google.com/file/d/1byZ6oRhqX_yaeKBGaa4wTF5QueqhAxUc/view?usp=sharing) |
| **EditGuard** | [Google Drive](https://drive.google.com/file/d/10PWPqLbfPUNrADgalwuSb3qzDQpXSlLx/view?usp=sharing) |
| **MBRS** | [Google Drive](https://drive.google.com/file/d/1q78pvr1RbUhH2G16aXDS3LY-Og2cndHv/view?usp=sharing) |

## 🖼️ Visualization

<div align="center">
<img width="1000" alt="image" src="figures/visualization.png?raw=true">
</div>

<div align="center">
Visual effects of the manipulations on the watermarked images.
</div>

## ✨ Quantitative comparison

<div align="center">
    <img width="1000" alt="image" src="figures/table.png?raw=true">
</div>

<div align="center">
Robustness Evaluation: Resisting Intra-model MEA.
</div>

