# Machine Learning Explainability Projects

This repository contains two Jupyter notebooks demonstrating explainability techniques for machine learning models:

## Projects

### 1. Heart Disease Prediction with SHAP (`heart_disease_llm.ipynb`)
- **Model**: XGBoost Classifier
- **Dataset**: Heart disease dataset with 14 features
- **Explainability**: SHAP (SHapley Additive exPlanations) values
- **Features**: 
  - Grid search hyperparameter optimization
  - Cross-validation for model evaluation
  - SHAP visualizations (waterfall, summary, bar plots)
  - Integration with Hugging Face LLM for explanations

### 2. X-ray Classification with LIME (`lime_xrayclassification-pg.ipynb`)
- **Model**: VGG16 transfer learning for medical image classification
- **Dataset**: X-ray images (COVID-19, Pneumonia, Normal)
- **Explainability**: LIME (Local Interpretable Model-agnostic Explanations)
- **Features**:
  - Pre-trained VGG16 with custom classification layers
  - Image preprocessing and data augmentation
  - LIME visualizations highlighting important image regions

## Requirements

### Python Dependencies
```
tensorflow
keras
xgboost
scikit-learn
pandas
numpy
matplotlib
seaborn
shap
lime
PIL
langchain-huggingface
```

### Installation
```bash
pip install -r requirements.txt  # (requirements.txt to be created)
```

## Usage

1. **Heart Disease Model**: 
   - Ensure `heart.csv` dataset is in the project directory
   - Set environment variables for Hugging Face API access
   - Run all cells in sequence

2. **X-ray Classification**:
   - Update file paths to point to your X-ray dataset
   - Ensure dataset has three folders: NORMAL, PNEUMONIA, Covid
   - Run all cells in sequence

## Security Notes

- Never commit API tokens or credentials to version control
- Use environment variables for sensitive configuration:
  ```bash
  export HUGGINGFACE_API_TOKEN="your_token_here"
  export HUGGINGFACE_REPO_ID="your_model_repo"
  ```

## Data Requirements

### Heart Disease Dataset
- CSV file with 14 features including age, sex, chest pain type, etc.
- Target variable indicating presence/absence of heart disease

### X-ray Dataset
- Organized in folders by class (NORMAL, PNEUMONIA, Covid)
- Images should be in common formats (JPEG, PNG)
- Recommended size: 224x224 pixels (will be automatically resized)

## Model Performance

- **Heart Disease**: Achieves >95% accuracy with proper hyperparameter tuning
- **X-ray Classification**: Achieves >96% validation accuracy using transfer learning

## Contributing

When contributing to this project, please ensure:
1. Code follows Python naming conventions
2. Sensitive information is properly handled via environment variables
3. Documentation is updated for new features
4. Models are properly validated before deployment