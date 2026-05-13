# MFGMNet: Multi‑Frequency Guided Matching Network for Optical‑SAR Image Registration

This repository contains the official implementation of our paper:

> **Accurate registration of optical and SAR images is challenged by nonlinear radiometric differences (NRDs), geometric distortions, and speckle noise, which compromise traditional methods. Although deep learning has improved registration performance to some extent through feature extraction, current deep learning methods still exhibit limitations in degraded feature representation under strong speckle noise and insufficiently discriminative feature embedding for matching.**
> 
> To address these issues, this paper proposes a **Multi‑Frequency Guided Matching Network (MFGMNet)** to achieve fast and robust matching of optical‑SAR images.

## 🚀 Key Ideas

- **Wavelet‑based frequency decomposition**  
  Shallow features are decomposed into four frequency sub‑bands (LL, LH, HL, HH) via Discrete Wavelet Transform (DWT).

- **Noise‑resistant cross‑attention**  
  A cross‑attention mechanism uses the noise‑resistant LL sub‑band to suppress speckle interference in the high‑frequency HH sub‑band.

- **Frequency‑Guided Channel‑Coordinate Attention (FGCCA)**  
  Before inverse DWT, the FGCCA module refines directional texture representations. Horizontal (LH) and vertical (HL) high‑frequency responses guide the attention, while channel‑spatial interdependence is decoupled to recalibrate features.

- **Coupled Circle Loss**  
  To obtain more discriminative feature embeddings, a novel coupled circle loss is introduced. Negative sample weights are conditioned on the average optimization difficulty of all positive samples, dynamically decoupling conflicting gradients between strong attraction and strong repulsion.

## 📊 Experimental Results

On the **OSdataset**, MFGMNet achieves:

- ✅ **≥ 28% improvement** in registration accuracy compared to state‑of‑the‑art methods.
- ✅ **~8.7% lower computational overhead** than the lightweight baseline RMSOConvNeXt.

These results demonstrate a highly efficient and robust solution for optical‑SAR remote sensing image registration.

## 📜 Code Availability

**The full source code will be made publicly available after the paper is accepted.**  
We are committed to open science and will release the code, pre‑trained models, and evaluation scripts under a permissive license (e.g., MIT) once the publication process is complete.

## 📝 Citation

If you find this work useful for your research, please consider citing our paper (citation details will be added upon acceptance).

```bibtex
@article{yourname2025mfgmnet,
  title   = {MFGMNet: Multi‑Frequency Guided Matching Network for Optical‑SAR Image Registration},
  author  = {Huatao Yu, Anxi Yu, Wenhao Tong, Yifei Ji, Zhen Dong},
  journal = {},
  year    = {2026},
  note    = {}
}
