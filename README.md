# 🔬 PathNet Tutorial: Multi-Scale CNN for Pathology Patch Classification

[![Python](https://img.shields.io/badge/Python-3.9-3776AB?logo=python)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.12-FF6F00?logo=tensorflow)](https://www.tensorflow.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-notebook-F37626?logo=jupyter)](https://jupyter.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A self-contained, runnable tutorial for building a patch-level histopathology
classifier in Python. **No real slide data required** — everything runs on
simulated H&E-like patches generated inside the notebook.

---

## What this teaches

Each section explains the *biological problem* first, then the *engineering
solution*, then *visualises the effect* of that solution:

| Section | Concept |
|---|---|
| 1 | Why H&E classification is harder than natural image classification |
| 2 | Simulating realistic H&E patches with class imbalance and scanner variation |
| 3 | Stain normalisation — Macenko SVD method, step by step |
| 4 | Squeeze-and-Excitation blocks — channel recalibration visualised |
| 5 | Multi-scale fusion — why 3×3/5×5/7×7 in parallel, and concat not sum |
| 6 | Spatial Attention Pooling — where is the model looking? |
| 7 | Learned Positional Encoding — giving the CNN a spatial memory |
| 8 | Class imbalance — Focal Loss explained with loss-landscape plots |
| 9 | Training PathNet with two-stage fine-tuning |
| 10 | Evaluation: optimal threshold, ROC curve, attention map overlays |

---

## Run immediately

```bash
# Install dependencies
pip install tensorflow numpy matplotlib scikit-learn opencv-python scipy

# Launch notebook
jupyter notebook PathNet_Tutorial.ipynb
```

Or open directly in Google Colab — click the badge above.

---

## What makes this a tutorial (not just code)

- **Simulated data** — generates 500 H&E-like patches in the notebook itself
- **Visual explanations** — every block has a before/after visualisation
- **"Why before how"** — each section opens with the biological motivation
- **Runs in one click** — no external datasets, no file paths to configure
- **Annotated code** — comments explain design decisions, not just syntax

---

## Companion repository

The production-ready codebase (real EfficientNetB0 backbone, WSI patch extraction,
two-stage fine-tuning, full MacenkoNormaliser) lives in:

👉 **[PathNet/](../PathNet)** — production codebase for real H&E slides

---

## Dependencies

All installed automatically by the first notebook cell:

```
tensorflow >= 2.10
numpy
matplotlib
scikit-learn
opencv-python
scipy
jupyter
```

---

## Author

**Hamed Abdollahi**
University of South Carolina // HA25@mailbox.sc.edu

---

## License

MIT License — see [LICENSE](LICENSE) for details.
