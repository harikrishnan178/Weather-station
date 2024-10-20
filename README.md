# Environmental Monitoring System using Raspberry Pi Pico

This project is an environmental monitoring system designed to measure and log various environmental parameters such as pressure, temperature, smoke, and gas levels (LPG, methane, hydrogen) along with accelerometer and gyroscope data using the Raspberry Pi Pico. The data is logged onto an SD card in real-time for further analysis.

# Features

Pressure and Temperature Measurement: Uses the BMP280 sensor to capture atmospheric pressure and temperature.
Gas Detection: Utilizes the MQ2 sensor to detect the presence of smoke, LPG, methane, and hydrogen gases.
Motion Detection: Incorporates the MPU6050 to monitor acceleration and angular velocity in 3 axes.
Data Logging: Logs all the collected sensor data into a CSV file on an SD card.

# Components Used

Raspberry Pi Pico: Microcontroller for managing the system.
BMP280 Sensor: For measuring atmospheric pressure and temperature.
MQ2 Sensor: For detecting smoke, LPG, methane, and hydrogen.
MPU6050: Accelerometer and gyroscope for motion detection.
Micro SD Card and SPI Interface: For data storage.
Connecting Wires: For circuit connections.
Breadboard/PCB: For assembling the components.

#How It Works

The system reads sensor data at regular intervals:
Pressure and temperature from BMP280.
Smoke, LPG, methane, and hydrogen levels from MQ2.
Acceleration and gyroscope data from MPU6050.
The data is logged into a CSV file (va.csv) stored on an SD card.
The collected data includes timestamps, allowing for time-based analysis.
# Software

The project is implemented in MicroPython. The script reads from the sensors and logs data to the SD card in real-time.

# Setup Instructions

Clone this repository:
bash
Copy code
git clone https://github.com/harikrishnan178/Weather-station
Install MicroPython on your Raspberry Pi Pico by following this guide.
Upload the main.py file to the Pico using Thonny or any other MicroPython IDE.
Connect the sensors and SD card module to the Raspberry Pi Pico as per the circuit diagram.

# Code Breakdown

i2c Configuration: Used to communicate with BMP280 and MPU6050 sensors.
SPI Configuration: Used for interfacing with the SD card module.
Data Logging: Data is logged in CSV format for easy analysis in tools like Excel or Python.

#Future Enhancements

Wireless Connectivity: Add Wi-Fi or Bluetooth modules for remote monitoring and real-time data visualization.
Additional Sensors: Include more environmental sensors for air quality, humidity, etc.
Power Optimization: Improve battery efficiency for longer usage in field applications.

# License

This project is licensed under the MIT License. See the LICENSE file for details.

# Acknowledgments

Special thanks to the open-source libraries and the MicroPython community for their contributions.
