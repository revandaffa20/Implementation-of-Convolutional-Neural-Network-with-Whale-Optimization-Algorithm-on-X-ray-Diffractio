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
|---|---|
| Baseline CNN | 84% |
| WOA-Optimized CNN | 91% |

## Repository Structure

| File | Description |
|---|---|
| `Pemrosesan_datamentah.ipynb` | Raw data processing. Contains the code for the initial processing of data obtained from CPICANN, used to filter the **ABX3 perovskite** entries. |
| `Prapemrosesan.ipynb` | Data preprocessing. Handles the **splitting** of the dataset (train/validation/test) before model training. |
| `EDA.ipynb` | Exploratory Data Analysis. Used for **graph visualization** of the data. |
| `Visualisasi_t_SNE.ipynb` | **3D t-SNE** visualization of the data/feature distribution. |
| `config.json` | Configuration file for model parameters, e.g. **batch size, epochs**, and other similar settings. |
| `modelling_CNN2.ipynb` | **Model training** of the 1D CNN, including its **evaluation**. |
| `Optimalisasi_WOA v2 copy.ipynb` | Runs the **WOA optimization of the CNN**, including its **evaluation**. |

### Workflow

1. `Pemrosesan_datamentah.ipynb`: filter ABX3 perovskite data from the CPICANN raw data
2.  `config.json`: set Configure parameters
3. `Prapemrosesan.ipynb`: split the data into train/validation/test sets
4. `EDA.ipynb`: explore and visualize the data
5. `modelling_CNN2.ipynb`: train and evaluate the baseline 1D CNN
6. `Optimalisasi_WOA v2 copy.ipynb`: run WOA-CNN optimization and evaluate the result
7. `Visualisasi_t_SNE.ipynb` : visualize the data 3D t-SNE

## Contribution

This method enables objective, reproducible, and accurate identification of crystal symmetry, and opens opportunities for application to other crystal systems and impurity analysis through XRD patterns.

## Keywords

`XRD` · `1D CNN` · `Whale Optimization Algorithm` · `Crystal Symmetry` · `Perovskite` · `Deep Learning`
