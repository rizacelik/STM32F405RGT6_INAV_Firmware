# STM32F405RGT6_INAV_Firmware
### New INAV Firmware Flight Controller

- **STM32F405RGT6**
* Freq: **168Mhz** Max
+ RAM: **192KB**
+ ROM:**1MB**

### PIN connections and details are as follows.
Click on the images to enlarge them.
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/8b158306-fe40-47d3-8212-c4da3251167f)
![image](https://user-images.githubusercontent.com/19993109/139479938-a1166d41-17c8-41a2-8903-195406ecd020.png)
## Supported sensors.
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/bed3cf62-04a1-4222-a3a9-800b1fce4415)

### EXAMPLE SPI2 SENSOR CONNECTION
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/97d98a0b-d53f-4c34-996b-af6201dd0c49)
Some of the sensors use the I2C bus. Some also use **SPI2** connection. You can connect one sensor for each of the **Gyro, Acc, Baro, Mag** sensors. For example, when you connect an **MPU6500**, you cannot use the **MPU6050**. The same is true for the **MPU9250**.
The following sensors use **SPI2** connection.

1. MPU6500
2. BMI160
3. BMI270
4. MPU9250
5. ICM42605

You can use one of these sensors.

### I2C SENSOR CONNECTION
You can also use I2C with multiple sensors as follows. You can use only one of the similar sensors in **I2C**.
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/ac09a49e-9fc3-4ae5-a6f5-f20ebfd3a4a2)

## Supported Internal MicroSD Card.
<img src="https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/e5053b6d-17c9-4ab2-8886-04f93c5f4f85" width=500>

## Supported Extranal OSD.
You can add OSD support using the MAX7456 chip by connecting it to the **SPI2** pins.
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/afa11087-5c00-4333-ad9e-c2061f642d7f)
![image](https://user-images.githubusercontent.com/19993109/244860476-c9fdb76d-98cc-43ad-b9f8-2bcff9c55686.png)

## RECEIVER Connection
You can connect the receiver of your transmitter to the **UART2** pin input as follows. You can use one of these receivers. For **SBUS** support, you need to use an inverter consisting of one transistor and two resistors.
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/473560cd-c581-4171-b584-23862973cc90)
Sbus receiver/Ibus receiver/PPM receiver please enable Serial RX for UART2
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/9cd678e9-067a-4170-aa8d-565eee2574c1)

## ESC and Motor connection
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/ca864895-37bf-425a-a290-dbeaacf6d94f)

## ESC and SERVO connection
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/a077e15a-7ba4-4781-8f35-a77e73413485)

## Motor, ESC and LIPO battery connection
The image below is an example of motor and LIPO battery connections. You need to connect the motor sequence according to the order shown in the "**INAV Configurator**" settings.
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/5203489a-7b2a-4838-9423-fe9953658346)

## Battery Monitor
To monitor the status of your LIPO Battery, you need to calculate the voltage divider according to the information given below and the battery power and connect it to the **VBAT_ADC_CHANNEL PC4 Pin**.
You should calculate the value that will enter a maximum of **3.3** volts on the **PC4 pin**. More than **5V** will damage the Board.
(Voltage Divider Calculator site:) https://ohmslawcalculator.com/voltage-divider-calculator
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/dbcd79ea-f3c2-4bb4-bee8-40f421e3a5a7)

## WS2811 5 Volt Led Strip
There must be a **5V** external voltage source. Don't buy from board source, you will burn the microcontroller.
![image](https://github.com/rizacelik/STM32F405RGT6_INAV_Firmware/assets/19993109/dfc2aa2c-cffe-4907-b29c-371563d3ef6a)
![image](https://user-images.githubusercontent.com/19993109/271059652-01d31dc0-9265-437c-8cec-c1dc0161a9a5.png)

## Calibration for ESC
Instructions for setting throttle calibration for ESC high and low signal input:
1. Connect the ESC with the motor, connect the signal lead to the board according to the pin and motor port according to the diagram. You should do this for all of the motors you are going to use.
2. Open the INAV Configurator and connect to the flight control hub.
3. Adjust the gyroscope / accelerometer and magnometer calibration settings.
4. Turn on the remote control and enable the receiver protocol in the Receiver section. 
5. Go to the Output field and set the ESC output protocol according to you. We describe the setup for the STANDARD protocol.
6.To calibrate ESCs, make sure the propellers are off, flick on the “I understand” toggle, raise Master to full value, and plug in your battery.
7. The ESCs will go through their tones.
8. When the double beeping sound is heard (the highest point of the throttle is confirmed), move the throttle to the lowest point.
9. ESC calibration is considered done when three beeps mean OK.
10. Now unplug, plug in again, and raise Master very slowly until the motors are spinning comfortably.

This video your can help. https://www.youtube.com/watch?v=1IrgbY0YhqM








