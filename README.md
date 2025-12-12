# ESPHome-Navien

ESPHome configuration for RS-485 control of Navien Hot Water Heaters.

## Status

**This repository contains example configuration only.** Active development has moved to the [htumanyan/navien](https://github.com/htumanyan/navien) ESPHome external component.

## Usage

This configuration uses the `htumanyan/navien` external component. To use it:

1. Copy `navien.yaml` to your ESPHome configuration directory
2. Create a `secrets.yaml` file with your credentials:
   ```yaml
   wifi_ssid: "your_wifi_ssid"
   wifi_password: "your_wifi_password"
   api_key: "your_api_encryption_key"
   ota_password: "your_ota_password"
   ```
3. Adjust GPIO pins (`tx_pin`, `rx_pin`) for your ESP32 board
4. Flash to your device: `esphome run navien.yaml`

## Hardware

- **Board**: ESP32 Dev (esp32dev)
- **Communication**: RS-485 to Navien water heater
- **Default Pins**: TX=GPIO19, RX=GPIO22

## Features

Provided by the [htumanyan/navien](https://github.com/htumanyan/navien) component:

- Temperature sensors (inlet, outlet, target)
- Water flow rate
- Gas usage tracking
- Power on/off control
- Recirculation ("Hot Button") control
- Climate entity for temperature adjustment

## Contributing

For issues or contributions related to the Navien component itself, please visit [htumanyan/navien](https://github.com/htumanyan/navien).
