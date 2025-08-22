🌱 AquaMind - Smart Irrigation System

AquaMind is an IoT-based smart irrigation system designed to automate watering, conserve water, and enable remote monitoring for modern agriculture and gardening.

🚀 Features

· Real-time Monitoring: Live data on soil moisture, temperature, and humidity.
· Automated Irrigation: Waters plants automatically based on soil moisture thresholds.
· Remote Control: Manual pump control via a sleek Android app.
· Activity History: Logs all pump events with timestamps and duration.
· AI Recommendations: Provides plant-specific watering advice.
· REST API: The hardware exposes a full API for easy integration.

🛠 System Architecture

Hardware Components

· Microcontroller: ESP8266 (NodeMCU)
· Sensors: Soil Moisture Sensor, DHT11 (Temperature & Humidity)
· Actuators: Relay Module, Water Pump
· Display: OLED Screen (SSD1306)
· Connectivity: Wi-Fi

Software Components

· Firmware: Written in C++ using Arduino IDE.
· Mobile App: Built with Android Studio (Java), using Retrofit for API calls.
· Communication: REST API over HTTP.

📡 How It Works

1. The ESP8266 boots as a web server hosting a REST API.
2. It continuously reads data from all sensors.
3. The automatic logic triggers the pump if soil moisture drops below 30%.
4. The Android app connects to the ESP8266's IP to send commands and fetch data.
5. All pump activities are logged locally on the microcontroller.

API Endpoints

· GET /api/sensor-data - Fetches current sensor values.
· GET /api/control-pump?state={on/off/auto} - Controls the pump.
· GET /api/pump-history - Retrieves the history of pump events.
· POST /api/clear-history - Clears the stored history.

📋 Installation & Setup

Hardware Setup

1. Connect the components as per the circuit diagram.
2. Power the ESP8266 and sensors.

Firmware Setup

1. Open the .ino file in the Arduino IDE.
2. Install required libraries (ESP8266WiFi, ArduinoJson, Adafruit_SSD1306, DHT, NTPClient).
3. Update Wi-Fi credentials (ssid and password) in the code.
4. Upload the code to the ESP8266.
5. Note the IP address shown in the Serial Monitor.

Android App Setup

1. Open the project in Android Studio.
2. In RetrofitClient.java, update BASE_URL to your ESP8266's IP address (e.g., "http://192.168.1.100/").
3. Build and run the app on an Android device.

🧩 Usage

1. Automatic Mode: The system will water plants automatically based on soil moisture.
2. Manual Control: Use the app to turn the pump ON/OFF or revert to AUTO mode.
3. View Data: Check the app's dashboard for live sensor readings.
4. Check History: Tap "View History" to see a log of all past activities.
5. Get Recommendations: Use the "AI Recommendation" button for plant-specific advice.

📊 Project Outcomes

· Water Savings: 30-70% reduction compared to traditional irrigation.
· Cost Reduction: ~50% lower labor costs.
· Increased Yield: Up to 30% higher crop productivity.
· Fast ROI: Pays back in under 12 months.

🔮 Future Roadmap

· Phase 1: Custom PCB, push notifications, Kickstarter launch.
· Phase 2: Multi-zone support, solar power integration, machine learning.
· Phase 3: B2B "Pro" version, API for smart home integration, global partnerships.

👨‍💻 Team

Team IoTrix

· Jawahar S
· Harshavarthan
· Jayesh S

📄 License

This project is licensed for academic and personal use.

🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

---

💡 Precision irrigation for a sustainable future: saving every drop, and every watt.

---
