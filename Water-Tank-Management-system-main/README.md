# Smart Water Quality Monitoring System (SWQMS)

An IoT-based water quality monitoring solution using ESP32, multiple sensors, Firebase Realtime Database, and a web-based dashboard.

## About The Project

The Smart Water Quality Monitoring System (SWQMS) is an IoT-based project developed to monitor important water quality parameters in real time.

The system uses an ESP32 microcontroller connected to multiple sensors to collect water-related measurements. The collected data is transmitted to Firebase Realtime Database and displayed through a web-based dashboard.

This project demonstrates the integration of IoT hardware, sensor data collection, cloud database technology, and web development.

## Key Features

- Real-time water quality monitoring
- ESP32-based sensor data collection
- TDS sensor readings
- Water turbidity monitoring
- Water temperature monitoring
- Firebase Realtime Database integration
- Live web-based monitoring dashboard
- Threshold-based warning indicators
- Recent sensor reading history

## Technologies Used

| Category | Technology |
|---|---|
| Microcontroller | ESP32 |
| Programming Language | C++ |
| Firmware Framework | Arduino |
| Frontend | HTML, CSS, JavaScript |
| Cloud Database | Firebase Realtime Database |
| Connectivity | Wi-Fi |
| Sensors | TDS, Turbidity, DS18B20 |

## Hardware Components

- ESP32 Development Board
- TDS Sensor Module
- Turbidity Sensor Module
- DS18B20 Temperature Sensor
- Breadboard and jumper wires
- Suitable power supply
- Wi-Fi connection

## System Architecture

1. Sensors collect water-related measurements.
2. ESP32 reads and processes sensor values.
3. ESP32 connects to the Wi-Fi network.
4. Sensor readings are transmitted to Firebase Realtime Database.
5. The web dashboard retrieves the stored sensor data.
6. Users can monitor the latest readings through the dashboard.

## Project Structure

```text
smart-water-quality-monitoring-system/
│
├── firmware/
│   └── esp32_swqms/
│       ├── esp32_swqms.ino
│       └── secrets.example.h
│
├── web-dashboard/
│   ├── index.html
│   ├── style.css
│   └── app.js
│
├── docs/
│   └── project-screenshots/
│
├── .gitignore
├── LICENSE
└── README.md
```

## Sensor Pin Configuration

| Sensor | ESP32 GPIO |
|---|---|
| TDS Sensor | GPIO 34 |
| Turbidity Sensor | GPIO 35 |
| DS18B20 Temperature Sensor | GPIO 4 |

## Getting Started

### Prerequisites

- Arduino IDE
- ESP32 board package
- Firebase account
- Required Arduino libraries
- Visual Studio Code (optional)
- Web browser

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-GITHUB-USERNAME/smart-water-quality-monitoring-system.git
```

### 2. Configure ESP32 Firmware

- Open the firmware/esp32_swqms directory.
- Create a private secrets.h file based on secrets.example.h.
- Configure your Wi-Fi credentials.
- Add your Firebase database configuration.
- Never upload private credentials to GitHub.

### 3. Install Required Libraries

Install the following libraries through Arduino IDE Library Manager:

- OneWire
- DallasTemperature

### 4. Configure Firebase

- Create a Firebase project.
- Enable Firebase Realtime Database.
- Configure appropriate database security rules.
- Add the required Firebase configuration to the firmware and web dashboard.
- Keep private credentials secure.

### 5. Upload ESP32 Firmware

- Connect your ESP32 board to your computer.
- Open esp32_swqms.ino using Arduino IDE.
- Select the correct ESP32 board and COM port.
- Compile and upload the firmware.

### 6. Run the Web Dashboard

- Open the web-dashboard directory.
- Configure Firebase settings in app.js.
- Run index.html using a local development server.
- Monitor the latest sensor readings through the dashboard.

## Monitoring Thresholds

The project currently uses configurable demonstration thresholds:

| Parameter | Threshold |
|---|---:|
| TDS | 500 ppm |
| Turbidity | 2500 raw sensor value |
| Temperature | 40 °C |

These values are project-defined warning thresholds and should not be considered official drinking-water safety standards.

Note: Turbidity readings are currently represented as raw sensor values and are not calibrated NTU measurements.

## Future Improvements

- Water quality history charts
- Improved sensor calibration
- Turbidity measurement in NTU
- Mobile application integration
- Email and mobile notifications
- User authentication
- Advanced data analysis
- Improved dashboard functionality

## Project Screenshots

Screenshots of the hardware setup, web dashboard, and Firebase database will be added here.

## Author

**Ruwin Kaushalya**

Software Engineering | IoT | Web Development

GitHub: https://github.com/ruwinkaushalya

## Disclaimer

This project is developed for educational and demonstration purposes. Sensor readings and warning thresholds do not provide official water quality certification or guarantee that water is safe for drinking.

## License

See the LICENSE file for licensing information.
