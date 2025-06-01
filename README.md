# PIbot 🤖 — A Multi-Modal Intelligent Robot Powered by Raspberry Pi

**PIbot** is an interactive desktop robot built on Raspberry Pi, combining computer vision, speech interaction, and gesture recognition. It can detect facial expressions, respond to voice commands, recognize hand gestures, and display dynamic emotions on a screen — making it an engaging and intelligent companion for daily use or educational purposes.

## 🌟 Key Features

- 🗣️ **Voice Wake-up and Dialogue**
  - Snowboy hotword detection for offline wake word recognition
  - Customizable voice interactions

- 😊 **Facial Expression Recognition**
  - Real-time face detection and emotion classification
  - Dynamic screen display for expressions like angry, happy, blink, neutral

- ✋ **Hand Gesture Recognition**
  - Recognizes gestures from 1 to 5
  - Each gesture triggers a specific robot action or expression

- 📺 **Emotion Display Interface**
  - Supports animated emotion faces on an integrated screen

- ⚙️ **Optimized for Raspberry Pi**
  - Efficient inference using Paddle Lite + OpenCV
  - NEON acceleration for faster image preprocessing

## 🧠 Gesture-to-Action Mapping

| Gesture | Action Description           |
|---------|------------------------------|
| 1       | Greet or wave                |
| 2       | stand up                     |
| 3       | lay                          |
| 4       | Blink or wink animation      |
| 5       | run forward                  |

## 🗂️ Project Structure
PIbot/
├── models/ # Face, gesture, and expression models
├── snowboy/ # Wake word detection module
├── src/
│ ├── main.cpp # Main robot control logic
│ ├── vision/ # Expression & gesture recognition
│ ├── voice/ # Voice wake and dialogue logic
│ └── display/ # OLED/LCD display handling
├── assets/ # Expression icons or animations
├── scripts/ # Deployment and launch scripts
└── README.md

## 🛠 Dependencies

- Paddle Lite
- OpenCV 4.5+
- Snowboy (local wake word engine)
- C++17
- Raspberry Pi OS
- LCD/OLED screen (I2C/SPI supported)

## ⚡ Quick Start

```bash
# Build the main program
cd src
mkdir build && cd build
cmake ..
make -j4

# Run PIbot
./PIbot

## photo
![PIbot Demo](assets/pibot.gif)
