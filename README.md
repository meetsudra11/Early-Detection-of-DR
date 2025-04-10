
## 🔍 Problem Statement
Diabetic Retinopathy is a serious eye condition caused by diabetes that can lead to blindness if not detected early. The goal of this project is to build an automated system to classify the severity of retinopathy from retinal fundus images.

## 🗂 Dataset
- **Source:** https://www.kaggle.com/datasets/ascanipek/eyepacs-aptos-messidor-diabetic-retinopathy/data
- **About Data:** This dataset is a unified of the Eyepacs, Aptos, Aptos (Gaussian Filtered) and Messidor Diabetic Retinopathy Datasets. This data set, consisting of a total of 92,501 jpg files, was created by combining the images in the public databases mentioned in the title and spliting randomly them into train (%80), validation (%10) and test (%10).

## 🛠 Tools and Technologies
- Python
- TensorFlow / Keras
- Scikit-learn (for SVM)
- OpenCV / PIL (for preprocessing)
- EfficientNet (TF Hub)
  
## ⚙️ Preprocessing Techniques
To improve the quality and uniformity of the input images, the following preprocessing steps were applied:
- **Cropping**: Removed black borders and focused on the retinal region.
- **Resizing**: Standardized all images to a fixed input shape suitable for EfficientNet-B5.
- **CLAHE (Contrast Limited Adaptive Histogram Equalization)**: Applied to enhance contrast on selected images.
- **Normalization**: Scaled pixel values to a 0–1 range.
- **Gamma Correction**: Adjusted image brightness to normalize illumination.
- **Sharpness Enhancement**: Boosted edge clarity for better feature extraction.

## 🧠 Model Architecture
We used a hybrid model for classification:
- **Feature Extractor**: Pre-trained **EfficientNet-B5** without the top layer to extract high-level features.
- **Classifier**: A **Support Vector Machine (SVM)** was trained on the extracted features to classify images into 5 classes.

## 📈 Results
- **Test Accuracy**: **79.83%**





