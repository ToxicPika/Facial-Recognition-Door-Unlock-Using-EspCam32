# Facial-Recognition-Door-Unlock-Using-EspCam32
Security is at most concern for anyone nowadays, whether it's data security or security of their own home. With the advancement of technology and the increasing use of IoT, digital door locks have become very common these days. Digital lock doesn’t require any physical key but it uses RFID, fingerprint, Face ID, pin, passwords, etc. to control the door lock. In past, we have developed many digital door locks applications using these various technologies. In this tutorial we build a Face ID controlled Digital Door lock system using ESP32-CAM.

The AI-Thinker ESP32-CAM module is a low-cost development board with a very small size OV2640 camera and a micro SD card slot. It has an ESP32 S chip with built-in Wi-Fi and Bluetooth connectivity, with 2 high-performance 32-bit LX6 CPUs, 7-stage pipeline architecture. We have previously explained ESP32-CAM in detail and used it to build a Wi-Fi door Video doorbell. This time we will use the ESP32-CAM to build a Face Recognition based Door Lock System using a Relay module and Solenoid Lock.

# Components Required
* ESP32 CAM
* FTDI Board
* Relay Module
* Solenoid Lock
* Jumper Wires
* Arduino UNO
* 12 Volt Battery Source 
# ESP32 CAM
The ESP32 CAM is a small, low-power camera module based on the ESP32-S chip. It features an OV2640 camera sensor, which is capable of capturing still images and video up to 1600x1200 resolution. The module includes a built-in Wi-Fi and Bluetooth module, making it easy to connect to other devices wirelessly. It is ideal for use in projects that require remote monitoring, security, or facial recognition.
![image](https://user-images.githubusercontent.com/96866038/222897209-20bad0be-7f68-4b03-9c48-a78ba8759937.png)

# FTDI Board
The FTDI board is a USB-to-serial adapter board that allows you to communicate with the ESP32 CAM module via a USB port. It provides a convenient way to program and debug the module without the need for an external programmer. The FTDI board includes a built-in USB interface and a 6-pin header that can be used to connect to the ESP32 CAM module.
![image](https://user-images.githubusercontent.com/96866038/222897232-e57b36fa-31ca-42db-8747-507331af728b.png)

# Relay Module
A relay module is an electronic switch that can be controlled by an electrical signal. It is used to turn on or off a high voltage or current device such as a solenoid lock or motor. The relay module typically includes several channels, allowing multiple devices to be controlled with a single module. It can be controlled by a microcontroller such as the Arduino UNO.
* This is a 5V, 5 Channel Relay Module PIN Diagram but we will use only One on them.
![image](https://user-images.githubusercontent.com/96866038/222897307-122450a0-432a-40ff-b912-6607c50adea0.png)

# Solenoid Lock
A solenoid lock is an electromechanical device that is used to lock or unlock a door or gate. It consists of a solenoid coil and a metal plunger that moves in and out of the coil when it is energized. The plunger is connected to a locking mechanism, allowing it to be locked or unlocked depending on the state of the solenoid. A solenoid lock can be controlled by a relay module and a microcontroller such as the Arduino UNO.
![image](https://user-images.githubusercontent.com/96866038/222897372-7a61898b-55ae-4329-b57e-8629eefcc407.png)

# Jumper Wires
Jumper wires are electrical wires that are used to connect components on a breadboard or circuit board. They are typically made of flexible wire with a male pin on each end, allowing them to be inserted into holes on the board. Jumper wires are useful for prototyping and testing circuits before they are soldered together.
![image](https://user-images.githubusercontent.com/96866038/222897395-c27813b0-bfef-43de-a6d9-eb2979886a08.png)

# Arduino UNO
The Arduino UNO is a popular microcontroller board that is used in many DIY electronics projects. It features an Atmel AVR microcontroller and includes a USB interface for programming and debugging. The board includes several digital and analog input/output pins that can be used to control other components such as the ESP32 CAM module, relay module, and solenoid lock.
![image](https://user-images.githubusercontent.com/96866038/222897426-2176a29a-7894-4953-8fad-74a05ce37956.png)

# 12 Volt Battery Source
A 12 volt battery source is used to provide power to the various components in a facial recognition system. It typically includes a rechargeable battery and a voltage regulator to ensure that the voltage is stable. A 12 volt battery source can be used to power the ESP32 CAM module, relay module, and solenoid lock, as well as other components in the system. It is ideal for use in projects that require mobility or where there is no access to a mains power source.
* I Have Used This as a 12V Battery Source but You can use anyother you have to provide specified voltages
![image](https://user-images.githubusercontent.com/96866038/222897580-05538f2c-16b1-45e1-aabf-dc1769fe356e.png)

# Programming EspCam32 using FTDI
![image](https://user-images.githubusercontent.com/96866038/222896459-30ba5306-4c78-4da5-a598-fc4c4160b861.png)
Programming the ESP32 CAM module using an FTDI board is a straightforward process that can be completed using the Arduino IDE. Here are the steps to follow:

1) Connect the FTDI board to your computer using a USB cable.
2) Connect the FTDI board to the ESP32 CAM module using jumper wires as follows:
3) Connect the FTDI board's ground pin to the ESP32 CAM's ground pin.
4) Connect the FTDI board's RX pin to the ESP32 CAM's TX pin.
5) Connect the FTDI board's TX pin to the ESP32 CAM's RX pin.
6) Connect the FTDI board's VCC pin to the ESP32 CAM's 5V pin.

# Install ESP32 Board on Arduino IDE
Here Arduino IDE is used to program ESP32-CAM. For that, first, install the ESP32 add-on on Arduino IDE.

1) To install the ESP32 board in your Arduino IDE, go to File> Preferences.
![image](https://user-images.githubusercontent.com/96866038/222896806-45af34ba-83a1-4a7e-98f0-7ff205464f28.png)

2) Paste This Link: https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
![image](https://user-images.githubusercontent.com/96866038/222896847-9678ec3f-73c9-49a0-8aad-a3c8cb23e712.png)

3) GOTO Tools > Board > Board Manager And Type "esp32" and Install board 1.0.4 as shown below
![image](https://user-images.githubusercontent.com/96866038/222896919-34beda3c-d5d3-4b98-a275-d73625d0d485.png)

4) Select the board details accordingly, Shown Below
![image](https://user-images.githubusercontent.com/96866038/222897119-38e08614-0638-4f01-ac1f-4a81f59fab77.png)

5) PORT: Select the attched port to your laptop/PC with your device. Can be any Depends on the port that is attaches to.
