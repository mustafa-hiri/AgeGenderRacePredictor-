# AgeGenderRacePredictor-
Creating a README for your project is a great way to introduce, explain, and guide users through your work. Here's a template based on the information provided about your project. You can customize it further to fit your project's specific details and requirements.

---

# Predictive Models for Age, Gender, and Race Classification

## Introduction

This project develops and implements predictive models using deep learning techniques to accurately classify age, gender, and race from facial images. Built upon the robust VGGFace model with a SENet50 backbone, these models are fine-tuned to offer high accuracy and performance. This initiative addresses the gap in available resources by not only providing the complete codebase but also the preprocessed datasets required for training and evaluation, ensuring reproducibility and transparency.

## Features

- **Age Prediction Model**: Utilizes regression techniques to estimate the age from facial features.
- **Gender Classification Model**: Binary classification model to distinguish between male and female.
- **Race Classification Model**: Multiclass classification model capable of identifying 5 distinct races: White, Black, Asian, Indian, and Others.

## Dataset Preprocessing

### Age and Gender Dataset
- Split into 80% training and 20% testing to ensure a balanced approach for model validation.
- Random allocation into train and test directories facilitates unbiased model training.

### Race Dataset
- Aimed at creating a balanced dataset to address class imbalances, especially reducing the 'White' category to 5,000 images.
- Encourages a more equitable model performance across diverse racial categories.

## Model Architecture

The models leverage the VGGFace model with a SENet50 architecture, including:
- Fine-tuning of the last layers to adapt to age, gender, and race classification tasks.
- Incorporation of dropout and batch normalization to enhance model generalization.

## Implementation

- **Optimizer**: Adam with a learning rate of 0.0001 for precise adjustments.
- **Loss Function**: Mean Squared Error for age prediction and categorical cross-entropy for gender and race classification.
- **Callbacks**: ModelCheckpoint and ReduceLROnPlateau to optimize training.

## Usage

The project includes detailed Jupyter notebooks (`model_age_regression.ipynb`, `model_gender_classification.ipynb`, `model_race_classification.ipynb`) demonstrating the entire process from dataset preparation, model training, to evaluation. Users are encouraged to follow these notebooks for a step-by-step guide.

## Requirements

- Python 3.x
- TensorFlow 2.x
- Keras
- VGGFace
- Other common data science libraries (NumPy, Pandas, Matplotlib)

## Installation

Clone this repository and install the dependencies:

```bash
git clone https://github.com/mustafa-hiri/AgeGenderRacePredictor-
cd AgeGenderRacePredictor-
pip install -r requirements.txt
```

## Contributing

Contributions, issues, and feature requests are welcome. Feel free to check [issues page] for a list of known issues or to report new ones.

## Acknowledgments

- Special thanks to the VGGFace project for providing the foundational model architecture.
- Gratitude towards the UTKFace dataset for enabling comprehensive model training and testing.
