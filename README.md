SEA:ME Pi Racer
-----------------------------------------------------------
# Table of Contents
- [Assemble Pi Racer](#assemble-pi-racer)  
- [Setup Raspberry Pi](#setup-raspberry-pi)  
    - [Connect PC & Raspberry Pi with Putty](#connect-pc--raspberry-pi-with-putty)
    - [Set up Raspberry Pi with Wiki](#set-up-raspberry-pi-with-wiki)
    - [Errors](#errors)

----------------------------------------

# Assemble Pi Racer
- Assemble the Pi-Racer following to the pdf
    - [Pi-Racer Wiki](https://www.waveshare.com/wiki/PiRacer_Pro_AI_Kit)
    - [Pi-Racer Pro AI Kit Tutorial pdf](https://www.waveshare.com/w/upload/a/a2/Piracer_pro_ai_kit-en2.pdf)  
> **Important Point** 
>> 1. When connect motor & servo, attention to the connection  
>> 2. Connect right direction the Camera

----------------
# Set up Raspberry Pi
## Install Raspberry Pi imager for set up Raspberry Pi
- [Download Imager in link](https://www.raspberrypi.com/software/)
    - Follow OS specific guide

## Write Image on Raspberry Pi  

###  Write downloaded Image on SD card
<img width="500" alt="image" src="https://user-images.githubusercontent.com/54701846/189227237-70456b2e-9adb-448b-a854-5b353e1934ef.png">  
  
- Operating System -> Downloaded image
- SD Card -> Your own SD card for Raspberry Pi

### Enable SSH & Setting WIFI
<img width="500" alt="image" src="https://user-images.githubusercontent.com/54701846/189228343-e1d0165b-3849-45f0-8a4c-28fc16b1b7ac.png">  

- Check **Enable SSH**
- Check **Set username and password**
    - Username is server's name
    - Password is server's password
    - **Remember this. It needs when connect Raspberry Pi server & PC**

![image](https://user-images.githubusercontent.com/54701846/189229057-2b93fa51-6bc7-49d2-bea5-63d155635273.png)  

- Check Configure wireless LAN
    - Enter the Wi-Fi or LAN information you are using on the PC you are connecting to

- Setting done. **Write the Image**

## Enable SSH
- Write finish and Move to **/boot** directory
- Enter the command ```touch ssh``` or ```touch /Volume/boot/ssh```
    - Second one only work in Linux or Mac

## Find & Connect Raspberry Pi

### 1st. Use monitor
1. Connect monitor with Raspberry Pi
2. Command ```ifconfig``` & check IP_ADDRESS
3. Command ```ssh -Y {SERVER_NAME}@{IP_ADDRESS}```

### 2nd. Use nmap
1. ```nmap -sn {IP_ADDRESS}.0/24 ```
    - ex) nmap -sn 192.168.2.0/24 -> Change last number to 0 or *
2. Find Raspberry Pi's IP_ADDRESS
3. Command ```ssh -Y {SERVER_NAME}@{IP_ADDRESS}```
> If there are many devices connected to the router, check the Raspberry Pie by turning it off and on

### 3rd. Make a wild guess
- Raspberry Pie IP is caught similar to a PC
> But I don't recommend it. It's not like a programmer.

## Install & Set up Environment
- Follow Step.6 to Step.12
    - [Reference Link](https://docs.donkeycar.com/guide/robot_sbc/setup_raspberry_pi/#step-6-update-and-upgrade)

--------------------

