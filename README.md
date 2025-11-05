# PETBot 3D Printer Firmware

This repository contains the customized Marlin firmware for the PETBot 3D printer.

## Based On

This firmware is based on an older version of the [Marlin](https://github.com/MarlinFirmware/Marlin) firmware, specifically a rewrite by Tonokip based on the Hydra-mmm firmware.

## PETBot Customizations

This firmware has been customized for the specific hardware and requirements of the PETBot. The key customizations are:

*   **PET Filament Preheat Settings:** The firmware includes preheat settings for two types of PET filament:
    *   **Clear PET:** 255°C
    *   **Green PET:** 245°C
*   **Extended Y-Axis:** The Y-axis has a significantly larger travel limit of 8000mm.
*   **Dual Z-Axis Stepper Drivers:** The firmware is configured to use two stepper drivers for the Z-axis, providing more stability and power for the Z-axis movement.
*   **RepRapDiscount Full Graphic Smart Controller:** The firmware is configured to use the RepRapDiscount Full Graphic Smart Controller, which provides an LCD interface for controlling the printer.

## Hardware Configuration

*   **Motherboard:** RAMPS 1.3 / 1.4
*   **Extruders:** 1
*   **Thermistors:** 100k EPCOS thermistors for both the hotend and the heated bed.
*   **LCD:** RepRapDiscount Full Graphic Smart Controller

## How to Build

1.  **Install Arduino IDE:** Download and install the [Arduino IDE](https://www.arduino.cc/en/software).
2.  **Install U8glib:** The `REPRAP_DISCOUNT_FULL_GRAPHIC_SMART_CONTROLLER` requires the `U8glib` library. You can install it by:
    *   Unzipping the `U8glib.zip` file located in the root of this repository.
    *   Copying the `U8glib` folder to your Arduino libraries directory (usually `Documents/Arduino/libraries`).
3.  **Open Marlin.ino:** Open the `Marlin/Marlin.ino` file in the Arduino IDE.
4.  **Select Board and Port:** In the Arduino IDE, go to `Tools > Board` and select `Arduino Mega 2560 or Mega ADK`. Then, select the correct serial port under `Tools > Port`.
5.  **Upload:** Click the "Upload" button to compile and upload the firmware to your printer's control board.

## Disclaimer

This firmware is highly customized for the PETBot 3D printer. It may not be suitable for other 3D printers without significant modifications. Use at your own risk.
