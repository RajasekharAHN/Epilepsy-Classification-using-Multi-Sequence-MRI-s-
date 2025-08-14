# Epilepsy Classification using Multi-Sequence MRI’s  

## 📌 Project Description  
**Epilepsy Classification using Multi-Sequence MRI’s** is a deep learning-based medical imaging project that automatically classifies brain MRI scans to detect epilepsy-related abnormalities. It processes multi-sequence MRI data through preprocessing, feature extraction, and convolutional neural network (CNN) models — including a custom CNN and transfer learning with Xception — to assist radiologists in early and accurate diagnosis.  
By automating this classification process, the system aims to reduce diagnostic delays, improve clinical decision-making, and support better patient outcomes.  

---

## 📑 Table of Contents  
- [Project Description](#-project-description)  
- [Installation](#-installation)  
- [Dataset Access](#-dataset-access)  
- [Usage](#-usage)  
- [Features](#-features)  
- [Technologies Used](#-technologies-used)  
- [How It Works](#-how-it-works)  
- [Frontend](#-frontend)  
- [Screenshots / Demos](#-screenshots--demos)  
- [Contributing](#-contributing)  
- [License](#-license)  
- [Credits / Acknowledgments](#-credits--acknowledgments)  
- [Contact](#-contact)  

---

## ⚙ Installation  

### Prerequisites  
- Python 3.8+  
- pip (Python package manager)  
- Jupyter Notebook / Google Colab  

### Steps  
1. **Clone the Repository**  
   ```bash
   git clone https://github.com/RajasekharAHN/Epilepsy-Classification-using-Multi-Sequence-MRI-s.git
   cd Epilepsy-Classification-using-Multi-Sequence-MRI-s
2. **Prepare Dataset**
   Download the MRI dataset (multi-sequence) from Kaggle as explained below in Dataset Access Section.
3. **Run the Notebook**
   open in Google Colab and run cell-by-cell.


## 📂 Dataset Access

This project uses a multi-sequence MRI dataset hosted on Kaggle.
### To access the dataset in Google Colab:
1. Upload your Kaggle API key (kaggle.json) to the Colab environment:
   ```bash
   from google.colab import files
   files.upload()  # Select the downloaded `kaggle.json` file from kaggle
2. Move the API key to the correct location:
   ```bash
   !mkdir -p ~/.kaggle
   !cp kaggle.json ~/.kaggle/
   !chmod 600 ~/.kaggle/kaggle.json
3. Download the dataset from Kaggle:
   ```bash
   ! kaggle datasets download -d masoudnickparvar/brain-tumor-mri-dataset --unzip
Note: never share kaggle.json file publicly as it contains your private Kaggle credentials.

### ⚠ Important:
The kaggle.json file contains your Kaggle API credentials (username and key) and must be kept private.
-Never upload it to a public repository.
-Never share it in screenshots or documentation.
-Store it locally on your machine or in a secure storage service.
-In public repos, use .gitignore to prevent it from being committed.
-If your credentials are exposed, regenerate the key from your Kaggle account settings immediately.

##🚀 Usage
1. Upload MRI images to the input directory.
2. Run the model training cells in the notebook.
3. Use the prediction function to classify MRI scans into relevant categories (e.g., epilepsy, non-epilepsy).
   ```bash
      prediction = model.predict(mri_image)
      print(prediction)

##🌟 Features
1. Multi-sequence MRI image classification.
2. Two models:
   - Transfer Learning with Xception.
   - Custom CNN designed from scratch.
3. Preprocessing pipeline for MRI normalization and augmentation.
4. Training, validation, and testing workflows in Jupyter Notebook.
5. Visualization of results and performance metrics.

## 🛠 Technologies Used
- Python
- TensorFlow / Keras
- NumPy, Pandas
- Matplotlib, Seaborn
- OpenCV (for image preprocessing)
- Streamlit (for web UI)
- Google Colab (for training)

## 🔍 How It Works
The project implements two models for MRI-based epilepsy and brain abnormality classification:
1. Transfer Learning (Xception)
   - Uses pre-trained Xception for feature extraction.
   - Fine-tuned on multi-sequence MRI dataset for epilepsy classification.
2. Custom CNN
   - Multi-layer convolutional architecture with pooling, dropout, and dense layers.
   - ~4.77M trainable parameters optimized for MRI image features.

3. Model Architecture – Custom CNN
This image shows the custom CNN structure with convolutional layers, pooling, dropout, and dense layers.
<img width="859" height="859" alt="image" src="https://github.com/user-attachments/assets/867b181d-e68d-4e24-9768-a346b6b408f9" />

## 🖥 Frontend
The project includes a Streamlit-based web application for real-time brain MRI classification.
Purpose: Provide an easy-to-use interface for uploading MRI scans and instantly viewing classification results.
**Features:**
- Drag-and-drop or browse to upload MRI images (JPG/PNG).
- Supports images up to 200MB.
- Displays predicted class with confidence score.
- Runs locally or via ngrok for remote access.

This shows the Streamlit interface with drag-and-drop upload for MRI scans.
<img width="940" height="429" alt="image" src="https://github.com/user-attachments/assets/f0988610-af30-496a-88af-709194f69c2a" />

## 🖼 Screenshots / Demos
**MRI Samples**
- Dataset Images
<img width="940" height="476" alt="image" src="https://github.com/user-attachments/assets/37af0600-5e61-4605-8e4e-979cfab064fa" />

- Training Dataset countplot
  <img width="1436" height="678" alt="image" src="https://github.com/user-attachments/assets/95345f68-4ecb-4416-9091-9a60df047f89" />
- Testing Dataset countplot
  <img width="1410" height="679" alt="image" src="https://github.com/user-attachments/assets/917357a9-2345-4240-b274-ccef09791a1b" />
  

**Model Training & Evaluation**
1. Transfer Learning (Xception)
   - Accuracy improvement over epochs
     <img width="940" height="341" alt="image" src="https://github.com/user-attachments/assets/6d69a7eb-dd34-4cba-8bbd-2fe00d0663c3" />
   -  Loss reduction over epochs
      <img width="940" height="294" alt="image" src="https://github.com/user-attachments/assets/cdd93c88-deda-442f-ba13-ea75840feff7" />
2. Custom CNN
   - Accuracy improvement over epochs
     <img width="940" height="328" alt="image" src="https://github.com/user-attachments/assets/62b663d4-0528-4cf1-8fb1-b55efe39836a" />
   - Loss reduction over epochs
     <img width="940" height="287" alt="image" src="https://github.com/user-attachments/assets/3dfe321e-060a-4bae-bc97-4a65b7bd576c" />
     

**Classification Results**

<img width="781" height="1108" alt="image" src="https://github.com/user-attachments/assets/914b7b2d-341d-4406-b868-259315e0c322" />
<img width="841" height="1169" alt="image" src="https://github.com/user-attachments/assets/8c02309a-9c80-4901-8cbe-8db851f63ee5" />
<img width="888" height="1170" alt="image" src="https://github.com/user-attachments/assets/c968e45d-51b5-47a9-9da0-c17ee6159a2c" />

**Confusion Matrix**
<img width="940" height="812" alt="image" src="https://github.com/user-attachments/assets/855d4d18-1524-474c-9a3e-17e787552b15" />

**Frontend Images**
<img width="940" height="656" alt="image" src="https://github.com/user-attachments/assets/3aaff7e4-64b9-44cc-8ba3-79fd3f09a561" />
<img width="940" height="788" alt="image" src="https://github.com/user-attachments/assets/9b379c1a-c261-4ca4-9fc5-fa22d129d3cd" />
<img width="940" height="460" alt="image" src="https://github.com/user-attachments/assets/8c026ab2-93e2-469b-8b71-8523c8f88be4" />

## 🤝 Contributing
- Contributions are welcome!
- Fork the repository.
- Create a feature branch.
- Commit your changes.
- Submit a pull request.

## 📜 License
This project is licensed under the MIT License – see the LICENSE file for details.

## 🙏 Credits / Acknowledgments
- Dataset providers and open-source MRI collections.
- TensorFlow/Keras for deep learning framework.
- Medical experts who provided feedback during model design.

## 📬 Contact
**Author:** Alamanda Hima Naga Rajasekhar
📧 Email: himanthalamanda03@gmail.com









