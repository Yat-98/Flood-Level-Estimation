
# Flood Level Estimation 📡🌊

This repository provides a proof-of-concept framework for detecting and estimating flood extents in aerial imagery using two deep-learning approaches: pixel-wise segmentation with U‑Net and patch-level classification with ResNet.

---

## 🗂 Repository Structure

```

Flood-Level-Estimation/
├── Research Papers/                    — vision & methods references
├── cropped\_car\_small.zip               — sample input images
├── cropped\_mask\_small.zip              — matching ground-truth masks
├── full\_bbox.csv                       — bounding boxes metadata
├── unet-with-classification.ipynb      — U‑Net semantic segmentation notebook
└── resnet-with-classification-prof.ipynb — ResNet-based flood patch classifier notebook

````

---

## ⚙️ What It Does

- **U‑Net Segmentation** (`unet-with-classification.ipynb`)  
  - Trains a U‑Net on image–mask pairs to generate pixel-level flood maps.
  - Visualizes predictions side-by-side with ground truth masks.

- **ResNet Classification** (`resnet-with-classification-prof.ipynb`)  
  - Fine-tunes ResNet to classify cropped image patches as “flooded” or “not flooded.”
  - Includes profiling of accuracy, precision, recall over a validation set.

---

## 🚀 Quick Start

1. **Clone the repo:**
   ```bash
   git clone https://github.com/Yat-98/Flood-Level-Estimation.git
   cd Flood-Level-Estimation

2. **Set up environment:**

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   pip install --upgrade pip
   pip install -r requirements.txt  # you may need to create this file
   

3. **Unzip sample data:**

   ```bash
   unzip cropped_car_small.zip
   unzip cropped_mask_small.zip
   ```

4. **Launch notebooks:**

   ```bash
   jupyter notebook
   ```

   Open and run:

   * `unet-with-classification.ipynb`
   * `resnet-with-classification-prof.ipynb`

---

## 📊 Results

* **U‑Net** yields visually accurate flood masks with strong pixel-wise performance.
* **ResNet** achieves high classification metrics (e.g., >90% accuracy, good precision and recall).



---

## 📚 References

* U‑Net: *Ronneberger et al. (2015)*
* ResNet Transfers: *He et al. (2016)*
* Included research papers in `Research Papers/`

---

## 🧭 Next Steps

* Scale to larger aerial datasets.
* Combine segmentation + patch classification for end-to-end flood monitoring.
* Serve flood maps via a lightweight Flask API or dashboard.

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

