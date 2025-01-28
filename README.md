# 🚗 **Driver Drowsiness Detection System** 🛣️

## **Overview**

The **Driver Drowsiness Detection System** is a cutting-edge solution aimed at **enhancing road safety** by **monitoring driver fatigue** in real-time. Leveraging advanced **deep learning techniques**, the system continually analyzes eye movements to detect signs of drowsiness and issues an alert to help prevent accidents.

---

## **✨ Key Features**

- **Real-time Monitoring**: 🔄  
  The system continuously captures and processes video feed from the webcam to monitor eye movements.

- **Deep Learning Model**: 🧠  
  A powerful **Convolutional Neural Network (CNN)** is trained to distinguish between **open** and **closed eye states**, enabling precise detection of drowsiness.

- **Alert Mechanism**: 🔔  
  If drowsiness is detected, the system triggers an **audible alarm**, ensuring the driver remains alert and focused.

---

## **📁 Project Structure**

```
Driver-Drowsiness-Detection-System/
├── Annotation/                     # Contains annotation files for the dataset
├── MRL Eye Dataset/                # Directory for the MRL Eye Dataset
│   └── mrlEyes_2018_01/            # Subdirectory with eye images
├── models/                         # Directory to save trained models
├── prepared data/                  # Processed data ready for training
├── Data Preparation.ipynb          # Notebook for data preprocessing
├── Model Training.ipynb            # Notebook for model training
├── main.ipynb                      # Main application notebook
├── alarm.wav                       # Audio file for alarm
├── best_model.h5                   # Best trained model file
├── haarcascade_frontalface_alt.xml # Haar Cascade for frontal face detection
├── haarcascade_lefteye_2splits.xml # Haar Cascade for left eye detection
├── haarcascade_righteye_2splits.xml# Haar Cascade for right eye detection
├── README.md                       # Project documentation
└── requirements.txt                # List of required Python packages
```

---

## **⚙️ Installation Guide**

### **Prerequisites**:

- **Python 3.7+**
- **Webcam** for real-time monitoring

### **Setup Instructions**:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Shubham-Singla259/Driver-Drowsiness-Detection-System.git
   cd Driver-Drowsiness-Detection-System
   ```

2. **Install Required Packages**:
   Ensure you have `pip` installed, and then run:
   ```bash
   pip install -r requirements.txt
   ```

3. **Download the MRL Eye Dataset**:
   - Download the dataset from the [MRL Eye Dataset](https://www.kaggle.com/datasets/abhinavmoudgil95/real-life-drowsiness-dataset) page on Kaggle.
   - Extract the dataset and place the `mrlEyes_2018_01` folder inside the `MRL Eye Dataset` directory.

4. **Run the Application**:
   Open and run the `main.ipynb` notebook in **Jupyter Notebook** or **Jupyter Lab**. The notebook will connect to your webcam, process the live video feed, and alert you if drowsiness is detected.

---

## **💻 Usage**

- **Data Preparation**:
  Use the `Data Preparation.ipynb` notebook to preprocess the **MRL Eye Dataset** images, resize them, normalize the pixel values, and split the data into training and testing sets.

- **Model Training**:
  The `Model Training.ipynb` notebook will guide you through training the **CNN model** on the processed data. After training, the model with the best performance is saved as `best_model.h5`.

- **Real-time Detection**:
  Run the `main.ipynb` notebook to start **real-time drowsiness detection** using your trained model. Ensure that your webcam is properly connected.

---

## **🤝 Contributing**

We welcome contributions from the community! If you have suggestions for new features, improvements, or enhancements, please feel free to **open an issue** or **submit a pull request**.

---

## **📜 License**

This project is licensed under the **MIT License**. Please refer to the `LICENSE` file for more information.

---

## **🙏 Acknowledgements**

- **MRL Eye Dataset**: Special thanks to the [MRL Lab](https://mrl.cs.vsb.cz/eyedataset) at **VSB-TUO** for providing the dataset used in this project.
  
- **Haar Cascade Classifiers**: The Haar Cascade classifiers used for face and eye detection are part of the **OpenCV** library.

---

**Stay Safe. Stay Alert. 🚗💤** 

