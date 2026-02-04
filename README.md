# ⚛️ SpectralMind: Atomic Spectroscopy Classification



> **Classifying atomic elements (Hydrogen, Helium, Neon, Argon) by analyzing spectral emission signatures with 100% accuracy.**


---

## 📋 Project Overview

**SpectralMind** implements and compares **Traditional Machine Learning** (SVM, Random Forest) and **Deep Learning** (PyTorch) approaches to identify atomic elements based on their unique spectral "fingerprints."

### 🎯 Objective
To correctly classify simulated spectroscopic data into four categories:
* **Hydrogen (H)**
* **Helium (He)**
* **Neon (Ne)**
* **Argon (Ar)**

---

## 📊 Dataset

We utilized a synthetic dataset representing realistic atomic emission spectra.

* **Source:** [Synthetic Atomic Spectrum Peaks](https://www.kaggle.com/code/alexzyukov/synthetic-atomic-spectrum-peaks-dataset-generation/input) by Alex Zyukov
* **Samples:** 1000 total spectra
* **Features:** 50 spectral intensity bands per sample
* **Classes:** 4 Balanced Classes
* **Data Split:** 60% Train, 20% Validation, 20% Test (Stratified)

---

## 🤖 Models Implemented

### 1. Support Vector Machine (SVM)
* **Kernel:** RBF
* **Hyperparameters:** `C=0.1`, `Gamma=scale`
* **Performance:** Fast training, perfect accuracy.

### 2. Random Forest
* **Configuration:** 50 Trees, Max Depth 10
* **Performance:** Robust baseline, perfect accuracy.

### 3. Deep Neural Network (PyTorch Lightning)
* **Architecture:** Feedforward Network (50 → 128 → 64 → 4)
* **Optimization:** Adam (lr=0.001) with Dropout (0.3)
* **Performance:** High-confidence predictions.

---

## 📈 Results Summary

| Model | Test Accuracy | Precision | Recall | F1-Score |
|:---|:---:|:---:|:---:|:---:|
| **SVM** | **1.0000** | **1.0000** | **1.0000** | **1.0000** |
| Random Forest | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| Deep Learning | 1.0000 | 1.0000 | 1.0000 | 1.0000 |

**🏆 Key Finding:** The spectral signatures for these elements are distinct enough that both simple and complex models achieve perfect separation. SVM is recommended for production due to its efficiency.

---

## 🛠️ Technologies Used

* **Language:** Python 3.12
* **ML Libraries:** `scikit-learn`, `PyTorch`, `PyTorch Lightning`
* **Data Processing:** `pandas`, `NumPy`
* **Visualization:** `matplotlib`, `seaborn`

---

## 🚀 How to Run

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/uutcurse/SpectralMind.git](https://github.com/uutcurse/SpectralMind.git)
    cd SpectralMind
    ```

2.  **Install dependencies:**
    ```bash
    pip install torch pytorch-lightning scikit-learn pandas numpy matplotlib seaborn
    ```

3.  **Run the notebook:**
    ```bash
    jupyter notebook project-2.ipynb
    ```

---

## 👤 Author

**Utkarsh Upadhyay**

[![GitHub] | (https://github.com/uutcurse)
[![LinkedIn] | (https://www.linkedin.com/in/utkarsh-upadhyay-881792273/)

---

## 📄 License

MIT License - feel free to use this project for educational purposes.

## 🙏 Acknowledgments

* **Alex Zyukov** for the synthetic dataset generation logic.
* **Kaggle Community** for resources and inspiration.
