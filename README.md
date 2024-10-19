# Pico-Rubber-Ducky
[Raspberry Pi Pico](https://thepihut.com/products/raspberry-pi-pico) is a small flexilbe microcontroller. In this case we'll be using it to create a small rubber ducky. There are some downsides to doing this rather than just buying the rubber ducky from HAK5, HOWEVER this is way more affordable. 

## Table of Contents 
[Hardware](#hardware) <BR>
[Important links](#important-links)<BR>
[Steps To Install](#steps-to-install)<BR>

## Hardware
To build this there are a few things you'll need:
1. A Raspberry Pi Pico
2. A USB data cable

## Important links
* https://circuitpython.org/board/raspberry_pi_pico/
* https://github.com/dbisu/pico-ducky

## Steps To Install
1. Go to [dbisu pico ducky github](https://github.com/dbisu/pico-ducky) and install the latest release from the realeases tab on the right hand side. You'll also need to clone the repo to get a local copy of the files -> git clone https://github.com/dbisu/pico-ducky.git
2. Download [CircuitPython](https://circuitpython.org/board/raspberry_pi_pico/) for the Raspberry Pi Pico. *Updated to 8.0.0, Download CircuitPython for the Raspberry Pi Pico W. *Updated to 8.0.0
3. Plug the device into a USB port while holding the boot button. It will show up as a removable media device named RPI-RP2. Holding the button is basically like a reset for the board.
4. Copy the downloaded .uf2 file to the root of the Pico. The device will reboot and after a second or so, it will reconnect as CIRCUITPY.
