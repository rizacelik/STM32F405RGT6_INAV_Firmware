# STM32F405RGT6_INAV_Firmware
New INAV Firmware Flight Controller

STM32F405RGT6
Freq: 168Mhz Max
RAM: 192KB, ROM:1MB

### PIN connections and details are as follows.
Click on the images to enlarge them.
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/8b158306-fe40-47d3-8212-c4da3251167f)

## Supported sensors.
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/bed3cf62-04a1-4222-a3a9-800b1fce4415)

### EXAMPLE SPI2 SENSOR CONNECTION
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/97d98a0b-d53f-4c34-996b-af6201dd0c49)
Some of the sensors use the I2C bus. Some also use SPI2 connection. You can connect one sensor for each of the Gyro, Acc, Baro, Mag sensors. For example, when you connect an MPU6500, you cannot use the MPU6050. The same is true for the MPU9250.
The following sensors use SPI2 connection.

MPU6500

BMI160

BMI270

MPU9250

ICM42605

You can use one of these sensors.
### I2C SENSOR CONNECTION
You can also use I2C with multiple sensors as follows. You can use only one of the similar sensors in I2C.
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/ac09a49e-9fc3-4ae5-a6f5-f20ebfd3a4a2)

## Supported Internal MicroSD Card.
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/e5053b6d-17c9-4ab2-8886-04f93c5f4f85)

## Supported Extranal OSD.
You can add OSD support using the MAX7456 chip by connecting it to the SPI2 pins.
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/afa11087-5c00-4333-ad9e-c2061f642d7f)
![image](https://user-images.githubusercontent.com/19993109/244860476-c9fdb76d-98cc-43ad-b9f8-2bcff9c55686.png)

## ESC and Motor connection

![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/ca864895-37bf-425a-a290-dbeaacf6d94f)

## ESC and SERVO connection

![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/a077e15a-7ba4-4781-8f35-a77e73413485)

## Motor, ESC and LIPO battery connection
The image below is an example of motor and LIPO battery connections. You need to connect the motor sequence according to the order shown in the "INAV Configurator" settings.
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/5203489a-7b2a-4838-9423-fe9953658346)

## Battery Monitor
To monitor the status of your LIPO Battery, you need to calculate the voltage divider according to the information given below and the battery power and connect it to the VBAT_ADC_CHANNEL PC4 Pin.
You should calculate the value that will enter a maximum of 3.3 volts on the PC4 pin. More than 5V will damage the Board.
(Voltage Divider Calculator site:) https://ohmslawcalculator.com/voltage-divider-calculator

![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/dbcd79ea-f3c2-4bb4-bee8-40f421e3a5a7)




