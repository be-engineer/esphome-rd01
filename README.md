ESPHome RD-01 mmWave Radar Sensor Custom Component

## Installation
Set wifi_ssid and wifi_password in your esphome's secrets.yaml first

1. Place rd01_uart.h into the components of your esphome configuration folder
2. Create new device with the yaml in this repository
3. Modify   tx_pin: TX and  rx_pin: RX to your pin define,such as tx_pin: GPIO15 rx_pin:GPIO13,do not use txd0 and rxd0(maybe used to usb port)
4. CHIP_EN of rd-01 can pullup to vcc.Can not tested with no RTS

## Wiring
ESP8266  | | RD-01
---------|-|-------|
3.3V    |<->| 3.3V
GND     |<->| GND
TX      |<->| GPIO7_RX
RX      |<->| GPIO16_TX
RTS     |<->| GHIP_EN
