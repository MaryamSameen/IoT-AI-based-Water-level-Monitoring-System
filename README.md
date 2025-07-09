# 💧 IoT + AI-based Water Level Monitoring System

This project is a smart water level monitoring system that combines IoT sensors with an AI model to track and predict water usage in a tank. It uses an ultrasonic sensor for real-time level detection and a machine learning model to forecast usage patterns. The system also features alerts, automatic motor control, and data logging with cloud integration.

---

## 📌 Features

- Real-time water level detection using an ultrasonic sensor
- Automatic motor ON/OFF based on water levels
- AI model for predicting future water usage patterns
- Alerts for low and high water levels (with buzzer/LED)
- OLED display to show current level and status
- Logs data to InfluxDB and visualizes it using Grafana

---

## 🧠 Components Used

- ESP32 / ESP8266 Microcontroller
- HC-SR04 Ultrasonic Sensor
- Relay Module (for pump control)
- Buzzer and LEDs (for alerts)
- OLED Display (I2C)
- WiFi (for cloud communication)

---

## ⚙️ Software Stack

- Arduino IDE (Embedded Code)
- Python (for ML training + prediction)
- TensorFlow Lite (for edge AI inference)
- InfluxDB + Grafana (for cloud logging and visualization)
- MQTT (for communication between ESP and backend, if used)

---

## 📂 Project Structure

![image](https://github.com/user-attachments/assets/e3937ad0-e145-4827-a189-b80db62a120a)


---

## 🛠️ Setup Instructions

### 🔧 Hardware

1. Connect the HC-SR04 sensor to the ESP32.
2. Attach the relay to control a water pump.
3. Wire up the buzzer, LED, and OLED display.
4. Power the system via USB or battery.

### ⚙️ Software

1. Upload the Arduino `.ino` code to ESP32 using Arduino IDE.
2. Train and convert the ML model to `.tflite` using Python.
3. Integrate the `.tflite` model into the ESP code (via array header).
4. (Optional) Setup InfluxDB + Grafana for data visualization.

---

## 📊 Example Outputs

- OLED shows: `Water Level: 35% | Motor: ON`
- Grafana dashboard with real-time level graph
- Buzzer alerts when level < 10% or > 90%

---

## 🧠 AI Model (Optional)

- Features: Timestamp, current level, previous usage
- Model: Trained in Python using historical usage data
- Deployed as `.tflite` on ESP32 for on-device inference

---

## 📸 Screenshots

_Add screenshots of OLED, buzzer alert, and Grafana chart here (optional)._

---

## 📜 License

This project is licensed under the MIT License.

---

## 🙋‍♀️ Author

**Maryam Sameen**  
GitHub: [@MaryamSameen](https://github.com/MaryamSameen)

---

## 💡 Future Enhancements

- Add mobile app integration using Blynk or Firebase
- Use capacitive sensor for more accurate readings
- Integrate cloud-based AI predictions

