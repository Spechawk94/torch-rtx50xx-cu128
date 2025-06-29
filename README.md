🇬🇧 [English version here](README_en.md)

# PyTorch 2.9.0 + CUDA 12.8 pour RTX 50xx (SM_120)

Ce dépôt fournit un `.whl` précompilé de PyTorch 2.9.0 (branche `main`) avec support CUDA 12.8, optimisé pour les GPU Ada Lovelace RTX 5080 / 5090 / 5070Ti (SM_120).

## ✅ Compatibilité

| Élément      | Spécification                     |
|--------------|------------------------------------|
| OS           | Ubuntu 22.04 / Pop!_OS 22.04       |
| Python       | 3.10 (cp310)                       |
| CUDA Toolkit | 12.8 (installé localement, sans driver) |
| GPU supporté | RTX 5080 / 5090 / 5070Ti (SM_120)  |

---

## 📦 Installation

1. Installez le toolkit CUDA 12.8 depuis NVIDIA :  
👉 https://developer.nvidia.com/cuda-12-8-0-download-archive  
**⚠️ Ne pas installer le driver si vous êtes sur Pop!_OS / System76.**

2. Installez le `.whl` :

```bash
pip install https://github.com/Spechawk94/torch-rtx50xx-cu128/releases/download/v2.9.0-cu128-rtx50xx/torch-2.9.0a0+git959dd0-cp310-cp310-linux_x86_64.whl
```

---

## 🧪 Vérification

```python
import torch
print(torch.__version__)
print(torch.version.cuda)
print(torch.cuda.is_available())
print(torch.cuda.get_device_name(0))
```

---

## ❗️Support

Aucun support gratuit.  
Pour un build custom (autre Python, CUDA, GPU), contactez-moi en privé (support payant uniquement).

---

## 🧠 Pourquoi ce dépôt ?

NVIDIA ne fournit pas encore officiellement de support SM_120 / RTX 50xx dans les toolkits récents.  
Ce build permet d'exploiter à 100% les cartes RTX 50xx avec PyTorch + CUDA 12.8, sans compilation manuelle.

---

Made by [Spechawk94](https://github.com/Spechawk94)
