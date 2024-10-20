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
* https://docs.hak5.org/hak5-usb-rubber-ducky/ducky-script-basics/hello-world
* https://github.com/hak5/usbrubberducky-payloads

## Steps To Install
1. Go to [dbisu pico ducky github](https://github.com/dbisu/pico-ducky) and install the latest release from the realeases tab on the right hand side. You'll also need to clone the repo to get a local copy of the files -> git clone https://github.com/dbisu/pico-ducky.git
2. Download [CircuitPython](https://circuitpython.org/board/raspberry_pi_pico/) for the Raspberry Pi Pico. *Updated to 8.0.0, Download CircuitPython for the Raspberry Pi Pico W. *Updated to 8.0.0
3. Plug the device into a USB port while holding the boot button. It will show up as a removable media device named RPI-RP2. Holding the button is basically like a reset for the board.
4. Copy the downloaded .uf2 file to the root of the Pico. The device will reboot and after a second or so, it will reconnect as CIRCUITPY.
5. Download adafruit-circuitpython-bundle-8.x-mpy-YYYYMMDD.zip here and extract it outside the device.
6. Navigate to lib in the recently extracted folder and copy adafruit_hid to the lib folder on your Raspberry Pi Pico.
7. Copy adafruit_debouncer.mpy and adafruit_ticks.mpy to the lib folder on your Raspberry Pi Pico.
8. Copy asyncio to the lib folder on your Pico.
9. Copy adafruit_wsgi to the lib folder on your Pico.
10. Copy boot.py from your clone to the root of your Pico.
11. Copy duckyinpython.py, code.py, webapp.py, wsgiserver.py to the root folder of the Pico.
12. For Pico W Only Create the file secrets.py in the root of the Pico W. This contains the AP name and password to be created by the Pico W.
secrets = { 'ssid' : "BadAPName", 'password' : "badpassword" }
13. Find a script on the [HAK5 github](https://github.com/hak5/usbrubberducky-payloads)  or create your own one using Ducky Script and save it as payload.dd in the Pico. Currently, pico-ducky only supports DuckyScript 1.0, not 3.0.
14. Be careful, if your device isn't in setup mode, the device will reboot and after half a second, the script will run.

## Set Up Mode
To edit the payload, enter setup mode by connecting the pin 1 (GP0) to pin 3 (GND), this will stop the pico-ducky from injecting the payload in your own machine. The easiest way to do so is by using a jumper wire between those pins as seen bellow.
