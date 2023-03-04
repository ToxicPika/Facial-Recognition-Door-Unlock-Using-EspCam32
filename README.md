# Facial-Recognition-Door-Unlock-Using-EspCam32
Security is at most concern for anyone nowadays, whether it's data security or security of their own home. With the advancement of technology and the increasing use of IoT, digital door locks have become very common these days. Digital lock doesn’t require any physical key but it uses RFID, fingerprint, Face ID, pin, passwords, etc. to control the door lock. In past, we have developed many digital door locks applications using these various technologies. In this tutorial we build a Face ID controlled Digital Door lock system using ESP32-CAM.

The AI-Thinker ESP32-CAM module is a low-cost development board with a very small size OV2640 camera and a micro SD card slot. It has an ESP32 S chip with built-in Wi-Fi and Bluetooth connectivity, with 2 high-performance 32-bit LX6 CPUs, 7-stage pipeline architecture. We have previously explained ESP32-CAM in detail and used it to build a Wi-Fi door Video doorbell. This time we will use the ESP32-CAM to build a Face Recognition based Door Lock System using a Relay module and Solenoid Lock.

Components Required
ESP32 CAM
FTDI Board
Relay Module
Solenoid Lock
Jumper Wires
Solenoid Lock
A solenoid lock works on the electronic-mechanical locking mechanism. This type of lock has a slug with a slanted cut and a good mounting bracket. When the power is applied, DC creates a magnetic field that moves the slug inside and keeps the door in the unlocked position. The slug will retain its position until the power is removed. When the power is disconnected, the slug moves outside and locks the door. It doesn’t use any power in a locked state. To drive the solenoid lock, you would need a power source that can give 12V @ 500mA. 

Solenoid Door Lock

We previously used a solenoid lock to build an Arduino based RFID door lock.

Circuit Diagram
