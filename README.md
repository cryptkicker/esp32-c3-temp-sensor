
# Home Temperature Sensor Project

This project uses an **ESP32-S3 Super Mini** microcontroller and a **BME280 sensor** to create a home temperature, humidity, and pressure monitoring system. The collected data can be displayed locally or sent to a server for remote monitoring.

---

## Features
- Measures temperature, humidity, and atmospheric pressure.
- Low power consumption with the ESP32-S3 Super Mini.
- Connectivity options via Wi-Fi.
- Expandable for additional sensors or features.

---

## Hardware Components

1. **ESP32-S3 Super Mini**
2. **BME280 Sensor** (temperature, humidity, pressure)
3. Breadboard and jumper wires
4. 5V wall plug adapter
5. USB cable for programming and power
6. (Optional) Enclosure for the assembly

---

## Wiring Diagram

Refer to the wiring diagram below to connect the ESP32-S3 Super Mini and the BME280 sensor:

- **BME280 Pins**
  - VIN to ESP32 5V
  - GND to ESP32 GND
  - SCL to ESP32 GPIO22 (default I2C clock)
  - SDA to ESP32 GPIO21 (default I2C data)

*Note: Ensure proper connections as incorrect wiring can damage the components.*

### Wiring Diagram Image
(*Insert wiring diagram here*)

---

## Assembly Pictures

Include pictures of the following:
1. Individual components.
2. Assembled wiring setup on the breadboard.
3. Final assembly inside the enclosure (if applicable).

---

## Software Setup

1. Install ESPHome on your computer following the [ESPHome Getting Started Guide](https://esphome.io/guides/getting_started.html).
2. Create a new ESPHome project for the ESP32-S3 Super Mini.
3. Add the following configuration to a ESPHome secrets.yaml file:

```yaml
authentication_key: '<base64 32-byte key>'
ota_password: "<OTA_PASSWORD>"
wifi_password: "<WIFI_PASSOWRD>"
ap_fallback_password: "<AP_FALLBACK_PASSWORD>"
```

4. Review and change esp32-c3-bme280.yaml file as needed to your liking.
5. Upload the configuration to the ESP32-S3 using ESPHome by executing the following command.
```bash
esphome -s device_name workshop run device.yaml
```
6. Monitor the logs to verify the sensor data is being read correctly and it connects to your WIFI.

---

## Design

A custom 3D-printed enclosure is available to house the ESP32-S3 Super Mini and the BME280 sensor. You can find the design files on [Printables](https://www.printables.com/model/1124472-esp32-c3-temperature-sensor-enclosure).

---

## Changelog

### v1.0.0
- Initial release with basic functionality.
- Temperature, humidity, and pressure readings displayed via serial output.

---

## Future Enhancements
- Use BLE instead of WIFI
- Support battery operation

---

## License
This project is open-source and available under the MIT License.

---

Happy building! Feel free to contribute or suggest improvements to this project.
