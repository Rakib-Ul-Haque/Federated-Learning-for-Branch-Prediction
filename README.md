# Federated Learning for Branch Prediction

This repository contains the official implementation of the paper:

**"Federated Learning for Branch Prediction"**

---

👥 Authors

Rakib Ul Haque, Wei-Ming Lin, and Panagiotis (Panos) Markopoulos

University of Texas at San Antonio (UTSA)

## 📌 Overview

Modern processors increasingly face **emergent workloads**—previously unseen execution patterns that appear on a subset of devices and later propagate across systems. Traditional branch predictors struggle to generalize under such conditions, especially in **non-IID environments**.

This work introduces a **hardware-aware federated learning (FL) framework** for branch prediction that:

* Enables **collaborative learning across processors** without sharing raw execution traces
* Combines **federated offline pretraining** with **lightweight online adaptation**
* Maintains **strict hardware constraints** (latency, memory, power)
* Achieves **state-of-the-art accuracy** with a compact MLP model

---

## 🧠 Key Contributions

* Federated learning framework tailored for **branch prediction**
* Hybrid learning paradigm:

  * **Offline federated pretraining**
  * **Streaming online adaptation (no replay)**
* Hardware-efficient **Tiny MLP (2-cycle inference)**
* Extensive evaluation under:

  * IID and non-IID settings
  * Small-scale (6 clients) and large-scale (60 clients) federation
  * Emergent workload scenarios

---

The dataset used in this work is publicly available and can be downloaded from the following repository: https://utsacloud-my.sharepoint.com/:f:/g/personal/rakibul_haque_utsa_edu/IgBPvT2tZ1_JTpVUZRsdp5VcAUVZAKrnkQ31BUvunLSSwlA?e=T4Jrob

## 📊 Results Summary

* Federated pretraining significantly improves **global generalization**
* Online adaptation enables **fast personalization**
* Proposed Tiny MLP:

  * ✅ Highest accuracy across IID & non-IID
  * ✅ Stable under heterogeneity
  * ✅ **2-clock cycle inference latency**

---

## ⚡ Hardware Characteristics

| Metric            | Value    |
| ----------------- | -------- |
| Model Size        | ~30 KB   |
| Parameters        | 15,425   |
| Inference Latency | 2 cycles |
| Power Estimate    | ~0.93 mW |

---

## 📈 Supported Configurations

* CS (Cold Start)
* OA (Only Adaptation)
* LL (Local Learning)
* LL-OA
* FL (Federated Learning)
* **FL-OA (Proposed)**

---

## 🔐 Privacy

* No raw execution traces are shared
* Only model updates are exchanged
* Suitable for **privacy-sensitive and IP-constrained environments**

---

## 📌 Future Work

* Multi-seed statistical evaluation
* Hardware-level RTL implementation
* Adaptive communication strategies
* Scaling to larger and more diverse workloads

---

## 🤝 Acknowledgments

This work was supported by the NSF PARTNER project:
**"Neuro-Inspired AI for the Edge at UTSA (NAIAD)"** (Award No. 2332744)

---

## 📬 Contact

* Rakib Ul Haque — [rakibul.haque@utsa.edu](mailto:rakibul.haque@utsa.edu)

---

## ⭐ Notes

* This repository will be updated with final camera-ready results and scripts.
* Dataset release depends on benchmark licensing constraints.

---
