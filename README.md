# AgeGenderRace Predictor

## Introduction
The AgeGenderRace Predictor leverages deep learning to accurately classify a person's age, gender, and race from facial images. This project is built upon the robust VGGFace model with a SENet50 backbone, providing high accuracy and performance. It fills a crucial gap by offering both the complete codebase and the preprocessed datasets necessary for training and evaluation, ensuring transparency and reproducibility.

## Features
- **Age Prediction Model**: Utilizes regression techniques.
- **Gender Classification Model**: Binary classification for male and female distinction.
- **Race Classification Model**: Multiclass classification for identifying White, Black, Asian, Indian, and Others.

## Dataset Preprocessing
- **Age and Gender Dataset**: Split into 80% training and 20% testing, randomly allocated into respective directories.
- **Race Dataset**: Aimed at creating a balanced dataset by capping the 'White' category at 5,000 images.

## Model Architecture
The models incorporate fine-tuning of the last layers specific to each classification task, along with dropout and batch normalization to enhance generalization.

## Implementation
- **Optimizer**: Adam (learning rate: 0.0001).
- **Loss Functions**: Mean Squared Error for age prediction; categorical cross-entropy for gender and race classification.
- **Callbacks**: ModelCheckpoint and ReduceLROnPlateau.

## Accessing Data and Models
The trained models and datasets are available in the [Releases](https://github.com/mustafa-hiri/AgeGenderRacePredictor-/releases/tag/AgeGenderRace) section. This includes `saved_models_age`, `saved_models_gender`, and `saved_models_race` alongside the dataset used for training and validation.

### Using the Models and Data
After downloading, you can predict age, gender, and race with the models as follows:
```python
from tensorflow.keras.models import load_model

# Example for loading and using the age model
age_model = load_model('path/to/saved_models_age.h5')
# Follow similar steps for gender and race models
```
For detailed usage, including preprocessing and interpreting outputs, refer to the provided Jupyter notebooks.

## Installation
Clone the repository and set up the environment:
```bash
git clone https://github.com/mustafa-hiri/AgeGenderRacePredictor-
cd AgeGenderRacePredictor-
pip install -r requirements.txt
```

## Contributing
Contributions are welcome! Please feel free to fork the repository, make your changes, and submit a pull request. For any issues or feature requests, check the [issues page](https://github.com/mustafa-hiri/AgeGenderRacePredictor-/issues).

## Acknowledgments
- Thanks to the VGGFace project for the model architecture.
- The UTKFace dataset was invaluable for model training and testing.
