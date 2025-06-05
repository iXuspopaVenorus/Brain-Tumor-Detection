# Brain Tumor Classification with VGG16 (Transfer Learning)

This project applies **Transfer Learning using VGG16** to classify brain MRI images into two categories: **Tumor** and **No Tumor**. The goal is to build an accurate deep learning model that can assist in early detection of brain tumors from medical images.

## Dataset
The dataset consists of brain MRI scans labeled as either `yes` (tumor) or `no` (no tumor). Images are preprocessed and resized to `224x224` pixels to match the VGG16 input format.

## Project Pipeline
The complete workflow includes:

1. **Data Preprocessing**  
   - Load images and labels  
   - Resize to 224x224 pixels  
   - Normalize pixel values  
   - One-hot encode labels

2. **Data Augmentation**  
   - Use `ImageDataGenerator` for better generalization and reduced overfitting

3. **Model Construction**  
   - Import pre-trained VGG16 (without top layer)  
   - Add custom dense layers for binary classification

4. **Training**  
   - Use `binary_crossentropy` loss and Adam optimizer  
   - Monitor training/validation accuracy and loss

5. **Evaluation**  
   - Confusion Matrix  
   - Classification Report  
   - ROC Curve & AUC  
   - Accuracy/Loss plots per epoch  
   - Grad-CAM visualization to interpret model focus

6. **Prediction Visualization**  
   - Display sample predictions with true vs predicted labels

## Results
Achieved over **88% validation accuracy** after training for 10 epochs using transfer learning.

## Model Export
The trained model is saved as both:
- `brain_tumor_classifier.keras` 

## Tools & Libraries
- Python, TensorFlow, Keras
- OpenCV, Matplotlib, NumPy
- Scikit-learn (metrics and preprocessing)
