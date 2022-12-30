# FlyLure
Project for collecting in-situ accelerometer data of fishing flies

Files here require the Arduino IDE with relevant Adafruit firmware/drivers installed through the IDE. Essentially, just follow the adafruit guides for each of the components (ADXL345 and ItsyBitsyM0 Express) to get the skinny on all drivers. You'll also need to format the SPI flash as a Fat32 drive, follow the adafruit guides on that, it's real simple. 
Once you have those downloaded, you're going to need to download the circuitpython .UF2 file that corresponds to the ItsyBitsyExpressM0 so you can install circuit python on the microcontroller. Once that's on, the protocol for operation goes:
1. Install circuitpython using .UF2 file
2. Run Arduino Code (ForceAcquire_SDFatSave), disconnect the controller from the computer and let it run off battery power
3. Acquire force data
4. Plug microcontroller back in, double click the reset button to go into bootloader mode, move the .UF2 file back onto the drive 
5. Grab .txt file with data
6. Delete .txt file
7. Rinse and repeat
