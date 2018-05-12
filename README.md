# Analog_Devices_Arduino_590B_Emmulator
ADI/Linear Technologies offers an open-source "LinearLab Tools" set for using Python, MATLAB, LabVIEW, C, etc. to control a sizable set of Linear Technologies demo boards with the aid of various USB to PC bridge controllers.  ADI provides the DC590B USB Serial Controller for low-speed DAC boards (e.g. DC1096B w/ LTC2642 16/14/12-bit Vout DAC).  At times the control boards are not available.  The LT DC2606 (Linduino) is built on the Atmega328 uC, just like the Arduino UNO board.  This repository provides the complete set of files to use the readily available Arduino UNO to emmulate the DC590B and or DC2606 functionality.  These files are the exact files that come in the LinearLabTools set without edit.  Files were just pulled together into one repository so the Arduino IDE v1.8.4 could build the code base.


Disclaimer: This code was authored by ADI/Linear Technologies not myself. It should be noted that the UNO does not possess the buffers on the SPI lines like the DC590 or Linduino. These buffes allow the HW to adjust the voltage level of the bus. The Arduino UNO implements +5V logic and must be translated to work with peripherals that require a different voltage level.  FYI, most ADI/LT demo boards all the user to apply an external I/O reference.

Reference Links:

1). LinearLab Tools Download: http://www.analog.com/en/design-center/evaluation-hardware-and-software/evaluation-platforms/linearlab-tools.html

2). DC590B referece page: http://www.analog.com/en/design-center/evaluation-hardware-and-software/evaluation-boards-kits/dc590b.html#eb-overview

3). DC2606 (Linduino) reference page: http://www.analog.com/en/design-center/evaluation-hardware-and-software/evaluation-boards-kits/dc2290a-a.html


Usage:
  1. Embed the Arduino UNO with the "Arduino_UNO_DC590_Emmulator.ino" using the Arduino IDE v1.8.4 or later
  2. Obtain Python 2.7 (may work with more recent versions)
  3. Open Connect_to_arduino_DC590.py and note that one can send I2C or SPI transactions using ascii commands (UNO must be connected to PC    using USB cable).
  
  NOTE: All commands and functions are listed in the firmware.  One must edit the firmware to add/remove/modify uC command set and           functionality.
