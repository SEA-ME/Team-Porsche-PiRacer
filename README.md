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

# Setup Raspberry Pi
## Connect PC & Raspberry Pi with Putty
- Install Putty
    - [How to install Putty](https://phoenixnap.com/kb/how-to-install-putty-on-ubuntu)  
- Search Raspberry Pi's IP
    - Check your IP with ```ifconfig```
    - ```nmap -sn {ip-address.*}/24```
    - example of ip-address -> ```192.168.1.*/24```
- Connect Raspberry Pi with Putty  
    <img width="302" alt="image" src="https://user-images.githubusercontent.com/54701846/188981361-80694d57-b7ad-4eb5-9d38-2a99ce37ff63.png">
    - Write Raspberry Pi address and open
    > Occur error ```PuTTY: unable to load font "server:fixed"```   
    > Go to **Fonts**  
    > Change font another one

## Set up Raspberry Pi with Wiki
- [Reference to Set up](https://www.waveshare.com/wiki/DonkeyCar_for_Pi-Setup_Raspberry_Pi)

## Errors  

>  **In Step 2. Cannot install library**  
![image](https://user-images.githubusercontent.com/54701846/188976845-8995b6c9-bb0d-4015-ad91-839cbad836ce.png)  
    -  In 2nd line, install libqtgui4 & libqt4-test doesn't work

> **In Step 4. Cannot install tensorflow**  
    ``` pip install tensorflow==1.13.1```  
    - Cannot install tensorflow  
    - Cannot install without specifying the version  

