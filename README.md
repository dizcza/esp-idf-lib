# ESP-IDF Components library

[![Build Status](https://travis-ci.org/UncleRus/esp-idf-lib.svg?branch=master)](https://travis-ci.org/UncleRus/esp-idf-lib)
[![Docs Status](https://readthedocs.org/projects/esp-idf-lib/badge/?version=latest&style=flat)](https://esp-idf-lib.readthedocs.io/en/latest/)

Components for Espressif ESP32 [ESP-IDF framework](https://github.com/espressif/esp-idf)

Most of them ported from [esp-open-rtos](https://github.com/SuperHouse/esp-open-rtos).

## How to use

Clone this repository to some dir, e.g.:

```Shell
cd ~/myprojects/esp
git clone https://github.com/UncleRus/esp-idf-lib.git 
```

Add path to components in your project makefile, e.g:

```Makefile
PROJECT_NAME := my-esp-project

EXTRA_COMPONENT_DIRS := /home/user/myprojects/esp/esp-idf-lib/components

include $(IDF_PATH)/make/project.mk
```

See [GitHub examples](https://github.com/UncleRus/esp-idf-lib/tree/master/examples) or [GitLab examples](https://gitlab.com/UncleRus/esp-idf-lib/tree/master/examples).

## Documentation

If examples is not enough you can read autogenerated documentation: https://esp-idf-lib.readthedocs.io/en/latest/

## Components

| Component      | Description                                                             | License | Thread safety
|----------------|-------------------------------------------------------------------------|---------|---------------
| **i2cdev**     | I2C utilites                                                            | MIT     | Yes
| **ds1302**     | Driver for DS1302 RTC module                                            | BSD     | No
| **ds1307**     | Driver for DS1307 RTC module                                            | BSD     | Yes
| **ds3231**     | Driver for DS1337 RTC and DS3231 high precision RTC module              | MIT     | Yes
| **hmc5883l**   | Driver for HMC5883L 3-axis digital compass                              | BSD     | Yes
| **qmc5883l**   | Driver for QMC5883L 3-axis magnetic sensor                              | BSD     | Yes
| **onewire**    | Bit-banging one wire driver                                             | MIT*    | No
| **ds18x20**    | Driver for DS18B20/DS18S20 families of one-wire temperature sensor ICs  | BSD     | No
| **dht**        | Driver for DHT11, AM2301 (DHT21, DHT22, AM2302, AM2321), Itead Si7021   | BSD     | No
| **sht31x**     | Driver for Sensirion SHT3x digital temperature and humidity sensor      | BSD     | Yes
| **si7021**     | Driver for Si7013/Si7020/Si7021/HTU21D/SHT2x and compatible             | BSD     | Yes
| **bmp180**     | Driver for BMP180 digital pressure sensor                               | MIT     | Yes
| **bmp280**     | Driver for BMP280/BME280 digital pressure sensor                        | MIT     | Yes
| **bh1750**     | Driver for BH1750 light sensor                                          | BSD     | Yes
| **ultrasonic** | Driver for ultrasonic range meters, e.g. HC-SR04, HY-SRF05              | BSD     | No
| **pcf8574**    | Driver for PCF8574 remote 8-bit I/O expander for I2C-bus                | MIT     | Yes
| **pcf8575**    | Driver for PCF8575 remote 16-bit I/O expander for I2C-bus               | MIT     | Yes
| **tca95x5**    | Driver for TCA9535/TCA9555 remote 16-bit I/O expanders for I2C-bus      | BSD     | Yes
| **mcp23008**   | Driver for 8-bit I2C GPIO expander MCP23008                             | BSD     | Yes
| **mcp23x17**   | Driver for I2C/SPI 16 bit GPIO expanders MCP23017/MCP23S17              | BSD     | Yes
| **hd44780**    | Universal driver for HD44780 LCD display                                | BSD     | No
| **pca9685**    | Driver for 16-channel, 12-bit PWM PCA9685                               | BSD     | Yes
| **ms5611**     | Driver for barometic pressure sensor MS5611-01BA03                      | BSD     | Yes
| **hx711**      | Driver for HX711 24-bit ADC for weigh scales                            | BSD     | Yes
| **ads111x**    | Driver for ADS1113/ADS1114/ADS1115 I2C ADC                              | BSD     | Yes
| **pcf8591**    | Driver for 8-bit ADC and an 8-bit DAC PCF8591                           | BSD     | Yes
| **tsl2561**    | Driver for light-to-digital converter TSL2561                           | BSD     | Yes
| **tsl4531**    | Driver for digital ambient light sensor TSL4531                         | BSD     | Yes
| **max7219**    | Driver for 8-Digit LED display drivers, MAX7219/MAX7221                 | BSD     | Yes
| **tda74xx**    | Driver for TDA7439/TDA7439DS/TDA7440D audioprocessors                   | MIT     | Yes
| **mcp4725**    | Driver for 12-bit DAC MCP4725                                           | BSD     | Yes
| **encoder**    | HW timer-based driver for incremental rotary encoders                   | BSD     | Yes
| **ina3221**    | Driver for INA3221 shunt and bus voltage monitor                        | MIT     | Yes
| **ina219**     | Driver for INA219/INA220 bidirectional current/power monitor            | BSD     | Yes

## Credits

- [Andrej Krutak](https://github.com/andree182), developer of BH1750 driver
- Frank Bargstedt, developer of BMP180 driver
- [sheinz](https://github.com/sheinz), developer of BMP280 driver
- [Jonathan Hartsuiker](https://github.com/jsuiker), developer of DHT driver
- [Grzegorz Hetman](https://github.com/hetii), developer of DS18B20 driver
- [Alex Stewart](https://github.com/astewart-consensus), developer of DS18B20 driver
- [Richard A Burton](mailto:richardaburton@gmail.com), developer of DS3231 driver
- [Bhuvanchandra DV](https://github.com/bhuvanchandra), developer of DS3231 driver
- [Zaltora](https://github.com/Zaltora), developer of INA3231 driver
- [Bernhard Guillon](https://gitlab.com/mrnice), developer of MS5611-01BA03 driver
- [Pham Ngoc Thanh](https://github.com/panoti), developer of PCF8591 driver
- [Gunar Schorcht](https://github.com/gschorcht), developer of SHT3x driver
- [Brian Schwind](https://github.com/bschwind), developer of TS2561 and TSL4531 drivers


