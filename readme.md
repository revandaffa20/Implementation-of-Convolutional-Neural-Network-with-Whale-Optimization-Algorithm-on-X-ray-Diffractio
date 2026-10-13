<img width="463" height="475" alt="Screenshot 2026-10-05 232822" src="https://github.com/user-attachments/assets/34681127-f45b-40c8-8b7f-18cc3c28a37f" />


Source : [Bartel et al.,2019](https://www.science.org/doi/reader/10.1126/sciadv.aav0693)



# Crystal Symmetry Detection from XRD Patterns using a WOA-Optimized 1D CNN

Classification of crystal symmetry (**cubic, monoclinic, tetragonal, and orthorhombic**) from X-ray diffraction (XRD) patterns using a **one-dimensional Convolutional Neural Network (1D CNN)** whose hyperparameters are optimized by the **Whale Optimization Algorithm (WOA)**.

## Background
Diffraction peak overlap and pattern similarity lead to inaccurate lattice parameter readings, a process that depends heavily on manual analysis. This challenge is particularly relevant for **perovskite** materials, which are used in a wide range of applications and therefore require an accurate method for identifying their crystal symmetry.

## Dataset
The dataset is available on Hugging Face: [ersky/Classification-Crystal-Symmetry-Perovskite-using-Deep-Learning](https://huggingface.co/datasets/ersky/Classification-Crystal-Symmetry-Perovskite-using-Deep-Learning)

## Methodology
1. **Data augmentation** to balance the class proportions across crystal systems.
2. **Data splitting** into training, validation, and test sets.
3. **1D CNN** as the classification model.
4. **WOA** as an outer loop around the CNN, iteratively optimizing hyperparameters using a fitness function derived from validation performance.

## Results

| Model | F1-Score |
|-------|----------|
| Baseline CNN | 84% |
| WOA-Optimized CNN | **91%** |

## Contribution
This method enables objective, reproducible, and accurate identification of crystal symmetry, and opens opportunities for application to other crystal systems and impurity analysis through XRD patterns.

## Keywords
`XRD` · `1D CNN` · `Whale Optimization Algorithm` · `Crystal Symmetry` · `Perovskite` · `Deep Learning`
