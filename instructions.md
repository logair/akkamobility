# Instructions to assembly a LogAir monitor   

## Software
1. Make sure you have installed Arduino IDE for your Operative System from https://www.arduino.cc/en/Main/Software
2. Once installed, make sure you have the following libraries installed: BME280Spi, NeoGPS, SdFat, PMS, 
3. From the boards manager, install boards "STM32F1xx" by *stm32duino*
4. Choose Maple Mini board
5. Download logair.ino from this repository
6. Connect the device through USB to your computer, compile the code and upload.

*Important note: the bluepill boards we use in the workshop have a bootloader already installed - If you buy the board, you will have to install it following [this instructions](http://wiki.stm32duino.com/index.php?title=Burning_the_bootloader)*
## Hardware
Below you will find each component of LogAir with a table to connect pins of it to the bluepill and images. Please note that some connectors will be shared (e.g., bluepill only has 3 GND connectors, A5, A6 and A7 are shared between SD holder and BM280)
- STM32 microcontroller "bluepill"
![pins bluepill](http://wiki.stm32duino.com/images/thumb/1/19/STM32_Blue_Pill_top.jpg/700px-STM32_Blue_Pill_top.jpg)

- BME280 module for temperature and humidity sensing

| Bluepill     | BME-280| 
| -------------|--------|
| 3.3          | VCC    |
| G            | GND    |
| A5           | SCL    |
| A7           | BDA    |
| A4           | CSB    |
| A6           | SDO    | 

![bme280](https://i.postimg.cc/jdBjwLWz/bme280.jpg)

- PMS7003 module for particulate matter sensing

| Bluepill     | PMS7003| 
| -------------|--------|
| 5v           | VCC    |
| G            | GND    |
| B10          | RX     |
| B11          | TX     |

*Note: pins that are not in the table are not used*

![pms](https://proxy.duckduckgo.com/iu/?u=https%3A%2F%2Ftse4.mm.bing.net%2Fth%3Fid%3DOIP.ckF_KWTrvjBWry-5d1uPqADxEC%26pid%3DApi&f=1) ![pm2](https://proxy.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.picclickimg.com%2Fd%2Fl400%2Fpict%2F272619147557_%2FPMS7003-High-Precision-Laser-Dust-Sensor-PM10-PM25.jpg&f=1)

- SD holder module

| Bluepill     |SDholder| 
| -------------|--------|
| 3.3          | 3V3    |
| B0           | CS     |
| A7           | MOSI   |
| A5           | CLK    |
| A6           | MISO   |
| GND          | GND    |

![sd](https://proxy.duckduckgo.com/iu/?u=https%3A%2F%2Fi.imgur.com%2F2Ld8ASn.png&f=1)

- GPS module

| Bluepill     | GPS+BD | 
| -------------|--------|
| G            | GND    |
| 5v           | VCC    |
| A3           | TXD    |
| A2           | RXD    |

*Note: GPs models may differ but pins are always the same: TX to A3, RX to A2, GND and 5v*

![gps](https://proxy.duckduckgo.com/iu/?u=https%3A%2F%2Fcdn.shopify.com%2Fs%2Ffiles%2F1%2F1432%2F4386%2Fproducts%2F24_57_14608bd8-16e5-463e-ae1b-e0313292e393_grande.jpg%3Fv%3D1485189571&f=1)

- Bluetooth generic module HM-10

| Bluepill     | HM-10  | 
| -------------|--------|
| G            | GND    |
| 3.3          | VCC    |
| A3           | TXD    |
| A2           | RXD    |

![bt](https://i.postimg.cc/26dWTnWR/hm10.png)

- SD card
- Laser-cut acrylic case


