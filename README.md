# Obstacle Detection for Visually Impaired

This project aims to assist visually impaired individuals by detecting obstacles such as pedestrians and cars using a machine learning model deployed on an ESP-EYE camera.

## Setup Instructions

### Step 1: Collect Datasets
- Collect real-world datasets of pedestrians and cars for training.

### Step 2: Train FOMO Model
- Train the Faster Objects, More Objects (FOMO) model using the collected datasets.

### Step 3: Export Model as Arduino Library
- Export the trained model as an Arduino library suitable for running on the ESP-EYE camera.

### Step 4: Download ESP-EYE Camera Driver
- Download and install the driver for the ESP-EYE camera for Windows devices.

### Step 5: Setup Arduino IDE
1. Install the ESP32 Boards Manager:
   - Open the Arduino IDE (version 1.8 or higher).
   - Go to File > Preferences.
   - In the Preferences dialog, add the following URL to the "Additional Boards Manager URLs": https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
   - Click OK to save the settings.
2. Install the EloquentESP32CAM Library:
   - In the Arduino IDE, go to Tools > Board > Boards Manager.
   - Search for "esp32" and install "esp32 by Espressif Systems".

### Step 6: Run Arduino Library
1. Open the Arduino IDE.
2. Go to Sketch > Include Library > Add ZIP Library.
3. Navigate to the location of the ZIP file containing your model library and select it to install.

### Step 7: Upload Sketch to ESP-EYE Camera
- Connect the ESP-EYE-CAM to your computer using a USB port.
- Upload the sketch to the camera using the Arduino IDE.
- Open the serial monitor in the Arduino IDE to view the inference of the model.
