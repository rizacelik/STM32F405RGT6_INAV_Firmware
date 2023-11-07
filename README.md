# STM32F405RGT6_INAV_Firmware
New INAV Firmware Flight Controller

STM32F405RGT6
Freq: 168Mhz Max
RAM: 192KB, ROM:1MB

### PIN connections and details are as follows.
Click on the images to enlarge them.
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/8b158306-fe40-47d3-8212-c4da3251167f)

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




