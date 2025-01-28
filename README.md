# Driver Drowsiness Detection System

## Overview

The **Driver Drowsiness Detection System** is designed to prevent accidents by monitoring driver fatigue in real-time. Utilizing deep learning techniques, the system analyzes eye movements to detect signs of drowsiness and alerts the driver to ensure safety on the road.

## Features

- **Real-time Monitoring**: Continuously captures and analyzes eye movements using a camera.
- **Deep Learning Model**: Employs a trained convolutional neural network (CNN) to distinguish between open and closed eye states.
- **Alert Mechanism**: Triggers an audible alarm when drowsiness is detected to prompt driver alertness.

## Project Structure

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

## Installation

### Prerequisites

- Python 3.7 or higher
- A webcam for real-time monitoring

### Setup Steps

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Shubham-Singla259/Driver-Drowsiness-Detection-System.git
   cd Driver-Drowsiness-Detection-System
   ```

2. **Install Required Packages**:
   Ensure you have `pip` installed. Then, run:
   ```bash
   pip install -r requirements.txt
   ```

3. **Download the MRL Eye Dataset**:
   - The dataset is not included in the repository due to its size. You can download it from the [MRL Eye Dataset](https://www.kaggle.com/datasets/abhinavmoudgil95/real-life-drowsiness-dataset) page on Kaggle.
   - After downloading, extract the dataset and place the `mrlEyes_2018_01` folder inside the `MRL Eye Dataset` directory.

4. **Run the Application**:
   Open and run the `main.ipynb` notebook using Jupyter Notebook or Jupyter Lab. This notebook captures real-time video from your webcam, processes the frames to detect drowsiness, and triggers an alarm if drowsiness is detected.

## Usage

- **Data Preparation**:
  - Use the `Data Preparation.ipynb` notebook to preprocess the images from the MRL Eye Dataset. This includes resizing images, normalizing pixel values, and splitting the data into training and testing sets.

- **Model Training**:
  - The `Model Training.ipynb` notebook contains the code to train a CNN model on the prepared data. After training, the best model is saved as `best_model.h5` in the root directory.

- **Real-time Detection**:
  - The `main.ipynb` notebook utilizes the trained model to perform real-time drowsiness detection. Ensure your webcam is connected and functioning properly before running this notebook.

## Contributing

Contributions are welcome! If you have suggestions for improvements or new features, feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

## Acknowledgements

- The MRL Eye Dataset used in this project is provided by the [MRL Lab](https://mrl.cs.vsb.cz/eyedataset) at VSB-TUO.
- The Haar Cascade classifiers are part of the [OpenCV](https://opencv.org/) library.
