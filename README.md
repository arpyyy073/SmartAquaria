Smart Aquarium Capstone Project

This project is a Capstone Project focused on building a Smart Aquarium System using various sensors and actuators to automate and monitor the aquatic environment.

---

Components Used
Turbidity Sensor – Measures water clarity

pH Level Sensor – Monitors water acidity/alkalinity

DS18B20 Temperature Sensor – Measures water temperature

Servo Motor – Controls automatic fish feeding

Submersible Pump Motor – Manages water change system

---

Features
Wi-Fi Configuration – Easily connect to any Wi-Fi using captive portal

App-Controlled Feeding – Trigger fish feeding through the mobile app

App-Controlled Water Change – Remotely activate water cycling system

---

Arduino Libraries Used:

<WiFi.h> – Connects the ESP32 to Wi-Fi networks

<OneWire.h> – Enables communication with the DS18B20 temperature sensor

<DallasTemperature.h> – Reads temperature data from the DS18B20

<FirebaseESP32.h> – Connects and interacts with Firebase Realtime Database

<Preferences.h> – Saves and retrieves data (e.g., device settings) in flash memory

<WebServer.h> – Hosts a local web server for custom Wi-Fi setup or diagnostics


---

🔧 Installation & Usage Guide
Smart Aquarium System using ESP32

This section explains how to install, upload, and use the Smart Aquarium System on your ESP32 device.

STEP 1. Required Tools & Software
Arduino IDE (latest version recommended)

- ESP32 Board Package

Libraries (install via Library Manager or manually):

- WiFi.h (included with ESP32 board package)

- OneWire

- DallasTemperature

- FirebaseESP32 by Mobizt

- Preferences (built-in)

- WebServer (included with ESP32 package)

---

STEP 2. Wiring and Connections
Component	-- > ESP32 Pin
DS18B20	-- > GPIO 4
Turbidity Sensor -- >	GPIO 34
pH Sensor	-- > GPIO 35
Servo Motor (Feeder) -- >	GPIO 15
Water Pump (Relay) -- >	GPIO 14
GND/Power -- >	3.3V / GND

⚠️ Adjust pin numbers in the code if you use different wiring.

---

STEP 3. Firebase Setup
1. Go to Firebase Console

2. Create a project

3. Add a Realtime Database

4. Get your:

- Database URL

- API Key

- User UID

NOTE: THIS SETUP DEPENDS ON WHAT WILL YOU USE! (MYSQL,POSTGRESQL and so on..)

---

STEP 4. Upload Code to ESP32
- Open your .ino file in Arduino IDE

- Go to Tools > Board and select "ESP32 Dev Module"

- Connect your ESP32 via USB

- Select the correct COM Port

- Click Upload 

---

STEP 5. First-Time Wi-Fi Setup

- On first boot, ESP32 starts in Access Point Mode

- Connect your phone to ESP32-AP Wi-Fi

- A captive portal opens automatically

- Select your home Wi-Fi network and enter the password

- ESP32 will connect and save credentials

AND YOUR DONE!

---

STEP 6. Using the Mobile App
(Assuming you’ve built or are using a React-based web/mobile app linked to Firebase)

Feeding: Tap the Feed Fish button to activate the servo

Water Change: Tap the Start Water Change to run the pump

Monitor: View real-time sensor data like pH, temperature, and turbidity

---

> This project showcases practical applications of IoT and embedded systems in aquaculture.
