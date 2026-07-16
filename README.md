# 🌿 LeafVision: Intelligent  Plant Disease Detection using Transfer Learning and Grad-CAM



## 📌 Project Overview

Early detection of plant diseases is essential for improving crop yield and reducing agricultural losses. Manual inspection is time-consuming and may require expert knowledge.

LeafVision is an explainable deep learning project that automatically detects plant diseases from leaf images using Transfer Learning. The project compares the performance of EfficientNetB0 and ResNet50 and uses Grad-CAM to visualize the regions of the leaf that influence the model's predictions.


## ✨ Features

- 🌿 Plant disease classification from leaf images
- 🧠 Transfer learning using EfficientNetB0 and ResNet50
- 📊 Comparative performance analysis of both models
- 🔥 Explainable AI using Grad-CAM visualizations
- 📈 Model evaluation using Accuracy, Precision, Recall, and F1-Score
- 📉 Confusion Matrix and training performance plots

## 📂 Dataset

This project uses the **PlantVillage** dataset containing healthy and diseased leaf images from multiple crop species.

**Dataset Details**

- Number of classes: **38**
- Image type: RGB leaf images
- Task: Multi-class image classification
- Dataset split: Training, Validation, and Test sets


**Dataset Link:**  
https://www.kaggle.com/datasets/emmarex/plantdisease


## 📁 Project Structure

```text
LeafVision/
│
├── notebooks/
│   ├── 01_Dataset_Exploration.ipynb
│   ├── 02_EfficientNetB0_Training.ipynb
│   ├── 03_ResNet50_Training.ipynb
│   ├── 04_Model_Comparison.ipynb
│   └── 05_GradCAM_Visualization.ipynb
│
├── models/
│
├── outputs/
│   ├── plots/
│   ├── confusion_matrix/
│   ├── gradcam/
│   ├── comparison/
│   └── sample_predictions/
│
├── data/
│
├── README.md
├── requirements.txt
└── .gitignore
```

## 🧠 Models Used

This project compares two transfer learning models for plant disease classification.

### 1. EfficientNetB0
- Pretrained on ImageNet
- Fine-tuned for plant disease classification
- Lightweight and computationally efficient

### 2. ResNet50
- Pretrained on ImageNet
- Fine-tuned on the PlantVillage dataset
- Deep residual architecture for robust feature extraction

## 📊 Results

The performance of EfficientNetB0 and ResNet50 was evaluated using validation accuracy, validation loss, model size, number of trainable parameters, and inference time.

| Metric | EfficientNetB0 | ResNet50 |
|--------|---------------:|---------:|
| Validation Accuracy | **98.998%** | 98.782% |
| Validation Loss | **0.1258** | 0.1393 |
| Trainable Parameters | **4.39 Million** | 24.13 Million |
| Model Size | **31.5 MB** | 206.9 MB |
| Inference Time | 0.06894 s/image | **0.05843 s/image** |

### Key Findings

- EfficientNetB0 achieved the highest validation accuracy (**98.998%**) and the lowest validation loss (**0.1258**).
- EfficientNetB0 required only **4.39 million trainable parameters**, compared to **24.13 million** for ResNet50.
- The EfficientNetB0 model size (**31.5 MB**) was significantly smaller than ResNet50 (**206.9 MB**), making it more suitable for deployment on resource-constrained devices.
- Although ResNet50 achieved a slightly faster inference time, the difference was small.
- Considering its higher accuracy, lower validation loss, reduced model size, and lower computational complexity, **EfficientNetB0 was selected as the final model for plant leaf disease detection.**

## 🔥 Explainability using Grad-CAM

To improve model interpretability, Gradient-weighted Class Activation Mapping (Grad-CAM) was used to visualize the regions of the leaf image that contributed most to the model's predictions.

Grad-CAM generates heatmaps that highlight disease-affected areas, allowing users to verify that the model focuses on relevant symptoms rather than background features. This enhances transparency and increases confidence in the model's predictions.

### Sample Grad-CAM Visualizations

The following examples demonstrate how the model identifies disease-affected regions in different plant leaves.

> *(Grad-CAM images will be displayed here.)*

## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- OpenCV
- Scikit-learn
- Jupyter Notebook
- Kaggle

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/your-username/LeafVision.git
```

Navigate to the project directory:

```bash
cd LeafVision
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

## 🚀 Usage

1. Download the PlantVillage dataset.
2. Train either the EfficientNetB0 or ResNet50 model using the notebooks.
3. Evaluate the trained model on the test dataset.
4. Compare the performance of both models.
5. Run the Grad-CAM notebook to visualize model predictions.

## 🙏 Acknowledgements

- PlantVillage Dataset
- TensorFlow and Keras
- Kaggle for providing GPU resources
