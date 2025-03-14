# Zest_Radio_LoRa868

Zest_Radio_LoRa868 board support for Zephyr OS.

## Usage

This board enables the following component:

- [Semtech SX1262](https://www.semtech.fr/products/wireless-rf/lora-connect/sx1262) LoRa radio transceiver

:pushpin: This shield defines:

- the LoRa radio transceiver alias: `lora_X` to `sx1262_zest_radio_lora868_X`

:triangular_ruler: To use this shield:

- Update your device tree by adding the `ZEST_RADIO_LORA868(port)` macro to the `app.overlay` file.\
  Replace `port` with the number of the Zest_Core port to which the shield is connected, e.g.:

  ```c
  ZEST_RADIO_LORA868(1) /* Zest_Radio_LoRa868 connected to Zest_Core first port */
  ```

- Activate support for the shield by adding `--shield zest_radio_lora868` to the west command.
