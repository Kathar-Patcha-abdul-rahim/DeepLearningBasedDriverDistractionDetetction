# Deep Learning-Based Driver Distraction Detection

This repository contains the implementation of a deep learning-based system to detect driver distractions using Convolutional Neural Networks (CNNs). The goal of this project is to enhance road safety by recognizing common distracted driving behaviors and reducing the likelihood of accidents caused by inattention.

## Overview

Driver distraction is a leading cause of accidents on the road. This project aims to address this issue by developing a Driver Activity Recognition (DAR) system that classifies various distracted behaviors using deep learning techniques. The system identifies 10 common distracted driving activities such as texting, talking on the phone, and operating the radio.

## Project Structure

- **Dataset**: The [State Farm Distracted Driver Detection dataset](https://www.kaggle.com/competitions/state-farm-distracted-driver-detection/data) was used to train and test the model. It contains 22,500 labeled images representing 10 driver activities.
- **Models**:
  - **Pre-trained Models**: DenseNet121, VGG16, MobileNetV2
  - **Custom Model**: DARNET (Custom CNN architecture)
  - **Ensemble Learning**: Combines DenseNet121 and DARNET for improved accuracy.
- **Key Metrics**:
  - Test Accuracy: 99.24% (Ensemble model)
  - Test Loss: 0.0390 (DARNET)
  
## Features

- **Driver Behavior Classification**: Detects 10 common driver activities:
  1. Safe driving
  2. Texting (right hand)
  3. Talking on the phone (right hand)
  4. Texting (left hand)
  5. Talking on the phone (left hand)
  6. Operating the radio
  7. Drinking
  8. Reaching behind
  9. Hair and makeup
  10. Talking to passengers
- **Deep Learning Models**: Utilizes pre-trained models and custom CNN architectures.
- **Data Augmentation**: Applies techniques like rotation, flipping, and translation to improve model generalization.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/driver-distraction-detection.git
    cd driver-distraction-detection
    ```
2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Download the dataset:
   - Download the State Farm Distracted Driver dataset from [Kaggle](https://www.kaggle.com/competitions/state-farm-distracted-driver-detection/data) and place it in the `data/` directory.

4. Run the training script:
    ```bash
    python train.py
    ```

## Models

- **DenseNet121**: Pre-trained on ImageNet, fine-tuned for driver behavior detection.
- **VGG16**: Simple yet effective CNN architecture used for comparison.
- **MobileNetV2**: Designed for mobile and embedded systems, providing efficient real-time classification.
- **DARNET**: A custom CNN architecture developed for this project to improve classification accuracy.

## Results

The ensemble model combining DenseNet121 and DARNET achieved the highest accuracy of 99.24% in classifying distracted driver behaviors. The custom DARNET architecture performed exceptionally well with a test accuracy of 98.60%.

## Challenges and Future Work

- **Dataset Limitations**: The current dataset is captured in controlled environments. Expanding the dataset to include real-world conditions can further improve model generalization.
- **Real-time Processing**: Implementing this system in real-time requires optimizing model inference time.
- **Privacy and Ethical Concerns**: Addressing user privacy while monitoring driver activities will be crucial for widespread adoption.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue for any bugs or feature requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- Kaggle for providing the [State Farm Distracted Driver Detection dataset](https://www.kaggle.com/competitions/state-farm-distracted-driver-detection/data).
- [TensorFlow](https://www.tensorflow.org/) and [Keras](https://keras.io/) for the deep learning frameworks used in this project.
