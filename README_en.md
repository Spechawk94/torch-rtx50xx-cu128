# PyTorch 2.9.0 + CUDA 12.8 for RTX 50xx (SM_120)

This repository provides a precompiled `.whl` of PyTorch 2.9.0 (built from the `main` branch) with CUDA 12.8 support, optimized for Ada Lovelace GPUs: RTX 5080 / 5090 / 5070Ti (SM_120).

## ✅ Compatibility

| Component     | Specification                      |
|---------------|-------------------------------------|
| OS            | Ubuntu 22.04 / Pop!_OS 22.04        |
| Python        | 3.10 (cp310)                        |
| CUDA Toolkit  | 12.8 (installed locally, no driver) |
| GPU supported | RTX 5080 / 5090 / 5070Ti (SM_120)   |

---

## 📦 Installation

1. Install CUDA Toolkit 12.8:  
👉 https://developer.nvidia.com/cuda-12-8-0-download-archive  
⚠️ **Do not install the NVIDIA driver if you're using Pop!_OS / System76.**

2. Install the `.whl`:

```bash
pip install https://github.com/Spechawk94/torch-rtx50xx-cu128/releases/download/v2.9.0-cu128-rtx50xx/torch-2.9.0a0+git959dd0-cp310-cp310-linux_x86_64.whl
```

---

## 🧪 Quick test

```python
import torch
print(torch.__version__)
print(torch.version.cuda)
print(torch.cuda.is_available())
print(torch.cuda.get_device_name(0))
```

---

## ❗️ Support

This wheel is provided **as-is**, without free support.  
💬 For custom builds (other Python versions, CUDA versions, or GPU architectures), contact me privately — **paid support only**.

---

## 🧠 Why this exists

NVIDIA has not yet officially supported SM_120 / RTX 50xx in public toolkits.  
This build enables full compatibility with PyTorch + CUDA 12.8 without having to compile it yourself.

---

Made by [Spechawk94](https://github.com/Spechawk94)