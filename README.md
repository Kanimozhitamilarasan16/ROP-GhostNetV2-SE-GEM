# ROP-GhostNetV2-SE-GEM

## Overview

This repository presents a deep learning framework for the classification of Retinopathy of Prematurity (ROP) using retinal fundus images.

The primary objective of this project is to investigate the effectiveness of a lightweight GhostNetV2-based architecture enhanced with Squeeze-and-Excitation (SE) and Global Efficient Module (GEM) components for automated ROP classification.

The repository also includes implementations and experimental notebooks for several established convolutional neural network architectures to provide comparative evaluation.

## Models and Experiments

The following architectures are included in this project:

* GhostNetV2
* GhostNetV2 with SE and GEM
* ResNet18
* DenseNet121
* EfficientNetV2S
* ConvNeXt-Tiny
* Standardized baseline comparison

The primary architecture investigated in this work is GhostNetV2-SE-GEM.

## Repository Structure

```text
ROP-GhostNetV2-SE-GEM/
│
├── Baseline_Comparison_Standardized.ipynb
├── DenseNet121.ipynb
├── EfficientNetV2S.ipynb
├── GhostNetV2.ipynb
├── GhostNetV2_SeGeM.ipynb
├── Resnet18.ipynb
├── convNeXt_tiny.ipynb
├── .gitignore
└── README.md
```

## Dataset

This project uses the **HVDROPDB Datasets for Classification and Segmentation for Research in Retinopathy of Prematurity**.

The dataset was developed using retinal fundus images of premature infants screened at PBMA's H.V. Desai Eye Hospital, Pune, using RetCam and Neo imaging systems. The classification component contains ROP and Normal image categories.

### Official Dataset

**HVDROPDB — Mendeley Data**

https://data.mendeley.com/datasets/xw5xc7xrmp

**DOI:** 10.17632/xw5xc7xrmp.3

The current published dataset is Version 3. The dataset is distributed under the Creative Commons Attribution 4.0 International (CC BY 4.0) license.

The dataset should be downloaded directly from the official source. The original retinal images are not included in this repository.

## Dataset Components

The HVDROPDB collection includes:

* RetCam and Neo retinal fundus images
* ROP classification data
* Normal classification data
* Retinal structure segmentation data
* Expert-provided annotations for segmentation tasks

The segmentation component includes annotations for structures such as the optic disc, blood vessels, and demarcation line/ridge.

## Data Organization

After downloading the dataset, organize the data according to the directory structure expected by the corresponding notebooks.

Dataset paths may need to be updated in each notebook depending on the local environment.

Example:

```text
dataset/
├── ROP/
│   └── ...
└── Normal/
    └── ...
```

The exact directory structure should be adapted to the downloaded HVDROPDB classification dataset and the paths specified in the notebooks.

## Methodology

The project follows a standard deep learning workflow:

1. Dataset preparation
2. Image preprocessing
3. Training and validation split
4. Data augmentation
5. Model training
6. Validation
7. Performance evaluation
8. Comparative analysis

The GhostNetV2-SE-GEM architecture is evaluated against established deep learning architectures to assess its effectiveness for ROP classification.

## GhostNetV2-SE-GEM

The proposed architecture combines the following components:

### GhostNetV2

GhostNetV2 is used as the lightweight backbone for efficient feature extraction.

### Squeeze-and-Excitation

The SE mechanism performs channel-wise feature recalibration to emphasize informative feature representations.

### Global Efficient Module

GEM is incorporated to improve global feature representation and enhance the extraction of discriminative information from retinal images.

The combined architecture is designed to investigate the balance between classification performance and computational efficiency.

## Requirements

The notebooks are designed to run in a Python-based deep learning environment.

Typical dependencies include:

```text
Python 3.x
PyTorch
torchvision
NumPy
pandas
OpenCV
Pillow
Matplotlib
scikit-learn
Jupyter Notebook
```

The exact package versions may depend on the training environment used for each experiment.

## Usage

Clone the repository:

```bash
git clone https://github.com/KanimozhitamilArasan16/ROP-GhostNetV2-SE-GEM.git
```

Navigate to the project directory:

```bash
cd ROP-GhostNetV2-SE-GEM
```

Download the HVDROPDB dataset from the official Mendeley Data repository:

https://data.mendeley.com/datasets/xw5xc7xrmp

Configure the dataset path in the relevant notebook and execute the preprocessing, training, validation, and evaluation cells.

## Experimental Notebooks

| Architecture        | Notebook                                 |
| ------------------- | ---------------------------------------- |
| GhostNetV2          | `GhostNetV2.ipynb`                       |
| GhostNetV2-SE-GEM   | `GhostNetV2_SeGeM.ipynb`                 |
| ResNet18            | `Resnet18.ipynb`                         |
| DenseNet121         | `DenseNet121.ipynb`                      |
| EfficientNetV2S     | `EfficientNetV2S.ipynb`                  |
| ConvNeXt-Tiny       | `convNeXt_tiny.ipynb`                    |
| Baseline Comparison | `Baseline_Comparison_Standardized.ipynb` |

## Reproducibility

To reproduce the experiments:

1. Clone this repository.
2. Download the HVDROPDB dataset from the official source.
3. Configure the dataset paths.
4. Install the required Python dependencies.
5. Open the corresponding Jupyter notebook.
6. Execute the preprocessing and training pipeline.
7. Evaluate the trained model using the evaluation procedures provided in the notebooks.

Random seeds, preprocessing parameters, training configurations, and evaluation settings should be kept consistent when reproducing the reported experiments.

## Data and Privacy

The original retinal fundus images are intentionally excluded from this GitHub repository.

The dataset should be obtained directly from the official HVDROPDB source and used in accordance with its license and applicable data-use requirements.

No patient-related retinal images or sensitive medical data should be uploaded to this repository.

## Citation

If you use the HVDROPDB dataset, please cite the dataset and associated publication.

### Dataset

Agrawal, R., & Kulkarni, S. (2024).
*HVDROPDB Datasets for Classification and Segmentation for Research in Retinopathy of Prematurity*. Mendeley Data, Version 3.

DOI: https://doi.org/10.17632/xw5xc7xrmp.3

### Associated Publication

Agrawal, R., Kulkarni, S., et al.
*HVDROPDB datasets for research in retinopathy of prematurity.*

Data in Brief, 52, 109839, 2024.

DOI: https://doi.org/10.1016/j.dib.2023.109839

## License

The HVDROPDB dataset is distributed under the Creative Commons Attribution 4.0 International (CC BY 4.0) license. Dataset users should review the official license and dataset terms before using or redistributing the data.

The source code in this repository is provided for research and educational purposes. Unless otherwise specified, the dataset license does not automatically apply to the source code contained in this repository.

## Author

**Kanimozhi Tamil Arasan**

GitHub:
https://github.com/KanimozhitamilArasan16

## Acknowledgements

The authors acknowledge the contributors of the HVDROPDB dataset and PBMA's H.V. Desai Eye Hospital, Pune, for providing the dataset used in this research.

## Repository

https://github.com/KanimozhitamilArasan16/ROP-GhostNetV2-SE-GEM
