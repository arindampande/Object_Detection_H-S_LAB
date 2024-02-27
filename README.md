# Obstacle Detection for Visually Impaired

## Overview

This project aims to assist visually impaired individuals by detecting obstacles such as pedestrians and cars in real-time using a tiny machine learning (TinyML) model deployed on an ESP32-based camera. The model, trained using the Faster R-CNN (Faster Objects, More Objects) architecture, is optimized for efficiency and accuracy.

## Dataset Collection

- Real-world datasets of pedestrians and cars were collected to train the model. These datasets were annotated to provide ground truth labels for training.

## Model Training

- The FOMO model was trained using the collected datasets. This model is designed to detect objects quickly and accurately, making it suitable for real-time applications.

## Model Deployment

- The trained model was exported as an Arduino Library, allowing it to be easily deployed on the ESP-EYE Camera. This library is optimized for the ESP32 platform, ensuring efficient execution on the device.

## Setting Up the Environment

1. *Download ESP-EYE Camera Driver:* Download and install the driver for the ESP-EYE Camera on your Windows device.

2. *Install ESP32 Boards Manager:*
   - Open the Arduino IDE (version 1.8 or higher).
   - Go to File > Preferences.
   - In the Preferences dialog, find the "Additional Boards Manager URLs" field.
   - Add the following URL: https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
   - Click OK to save the settings.
   - Go to Tools > Board > Boards Manager.
   - Search for "esp32" and install the "esp32 by Espressif Systems" package.

3. *Install EloquentESP32CAM Library:* This library is required for interfacing with the ESP-EYE Camera in the Arduino IDE.

## Running the Model

1. *Include the Library:*
   - Open the Arduino IDE.
   - Go to Sketch > Include Library > Add ZIP Library.
   - Select the ZIP file containing your model library and install it.

2. *Upload the Sketch:*
   - Connect the ESP-EYE Camera to your computer via USB.
   - Select the ESP32 board from Tools > Board.
   - Select the correct port from Tools > Port.
   - Open the sketch that contains your model.
   - Click on the upload button to upload the sketch to the ESP-EYE Camera.

3. *Viewing the Inference:*
   - Open the Serial Monitor in the Arduino IDE to view the inference results from the model.

## Conclusion

By following these steps, you can deploy the obstacle detection model on the ESP-EYE Camera, enabling real-time detection of pedestrians and cars to assist visually impaired individuals in navigating their surroundings
