# Purpose
Sense pressure and temperature using Arduino.

# References
Adafruit BMP085

# Equipment
## Hardware
Arduino Duemilanove "2009"  

BMP085 Barometric Pressure/Temperature/Altitude Sensor- 5V ready
https://adafruit.com/products/391
Adafruit ID: 391

## Software libraries

### Adafruit_BMP085
https://github.com/adafruit/Adafruit-BMP085-Library
I expanded, changed dash to underscore
Put in Arduino/libraries/Adafruit_BMP085  

# Results
Copied file Adafruit_BMP085/examples/BMP085test/BMP085test.pde  
Opened in Arduino, it saved file in a folder as arduino_pressure_temp_sensor.
Arduino changed file extension from .pde to .ino  

## Hardware Connect
This version of the board can use between 3-5 V.
### IF CONNECTING A SECOND DEVICE TO THE I2C BUS THAT RUNS AT 3V, I THINK USING BMP AT 5V COULD DAMAGE THE 3V DEVICE.
"a 3.3V regulator and a i2c level shifter circuit is included so you can use this sensor safely with 5V logic and power"
https://adafruit.com/products/391#Description

For example, the luminosity sensor TSL2561 runs at 3.3 V.
"As long as all the sensors/device on the i2c bus are running on 3.3V power, we're fine.
However, don't use a 5.0v powered i2c device (like the DS1307) with pullups at the same time as a 3.3V device like the TSL2561"
http://learn.adafruit.com/tsl2561/wiring

| Sensor | Arduino Duemilanove Pin |
| ------ | ----------------------- |
| Vin    | 3V                      |
| GND    | GND                     |
| SCL    | 5                       |
| SDA    | 4                       |
