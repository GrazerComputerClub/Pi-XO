# Pi-XO
Raspberry Pi Zero game console for use with PICO-8 
The hardware and software is sill under development!  

## Errata

Rev. 01. board  error:
  - *Error:* Speaker- an audio amp. output- connected to GND.  
    *Solution:* Do not wire speaker and audio amp. output (PAD5 and PAD6) to PCB, please connect speaker to audio amp. output via wire.  
    *Drawback:* Headphone connector not working 
  - *Error:*  ADC input direct connected to batterie A result in applying ~0.6 V to 3.3 V supply if batterie is attached and device is off.  
    *Solution:* Do not assamble MCP3202 (IC1).  
    *Drawback:* No batterie monitoring possible.

## Features

- **Multiple display options** - 160x128 or 320x240   
- **Audio (speaker / handphone)**
- **Classic dual NiMH AA-Batterie supply**
- **Batterie monitoring**
- **GPIOs (LED bar)**
- **Vibration motors**
- **Low cost**

## OS installation

- Download latest Raspjamming-Image https://github.com/GrazerComputerClub/Raspjamming-Image and flash to SD card
- Unzip PICO-8-rasp.zip to boot partiton (Executabe needed pico-8/pico8) 
- Activate line 'include Pi-XO.txt' in config.txt file
- Activate correct Display Option 1-3 including resolution in Pi-XO.txt file 
   * Display 1: 320x240 Display mounted far right side 
   * Display 2: 160x128 Display mounted right side 
   * Display 3: 160x128 Display mounted left side 

## Functions

- Fn-Button and Up/Down-Button: Volume control
- Fn-Button and Left/Right-Button: Display brightness (Display 1 and 2)
- Fn-Button and P-Button: Shutdown


![PCB Top](https://github.com/GrazerComputerClub/Pi-XO/raw/master/Pi-XO.png)

![Pi-XO](https://github.com/GrazerComputerClub/Pi-XO/raw/master/Pi-XO.jpg)

# Assambling

## Components list
	
 1 x Female pin header socket 2x20  
 1 x Switch 3-pin (S9) - Device on/off  
 1 x 2Pin + Jumper or Switch 2-pin (S6)- Vibration motors on/off  
 8 x Tactile switch 6x6mm (S1-S7)  
 1 x Audio amplifier board PAM8302 (JP3, do not connect PAD5 and PAD6) - https://www.ebay.de/sch/i.html?_nkw=PAM8302  
 1 x DC/DC Step Up Converter to 3.7V (JP2)  
 1 x Speaker 8 Ohm (connect to amplifier board PAM8302 Output via wire) - https://www.neuhold-elektronik.at/catshop/product_info.php?products_id=6645  
 1 x LED bar 8 segments (align right site)  
 1 x Resistor array 1K (RN1)  
 2 x Vibration motor (JP4, JP5) - https://www.neuhold-elektronik.at/catshop/product_info.php?products_id=6971  
 2 x AA Batterie holder (needs DC/DC Step Up Converter) or Dual AAA Batterie holder (no DC/DC Step Up Converter needed) - https://www.reichelt.at/battery-holder-1x-mignon-aa-halter-1xaap-p113168.html  
 2 x BC547B transisior (T1, T2)  
 2 x BC557B transisior (Q2)  
 2 x Resistor 2K2 Ohm (Transistor base vibration motor: R1,R2)
 1 x Resistor 270 Ohm (Audio filter: R3)  
 1 x Resistor 150 Ohm (Audio filter: R4)  
 2 x 1K Ohm (R5, R6) - protection UART pin  
 1 x 1K (R7) - base resistor transisitor background LED display  
 2 x Capacitor 33 nF (C1, C5)  
 1 x Electrolytic capacitor 10 uF/6.3 V (C2)  
 1 x Electrolytic capacitor 300 uF/6.3 V (C6)  
 1 x MCP3202 (IC1, do not connect)  
 1 x Headphone connector (X2, do not connect) - https://www.reichelt.at/jack-socket-3-5-mm-pcb-with-switch-contact-ebs-35-p7301.html  
 2 x Diode 1N4001 (D2 or D4, D1 or D3)  
 1 x 1,8" Display 160x128 ST7735 11-pin (JP7) or 8-pin (JP11) - https://www.ebay.de/sch/i.html?_nkw=1.8+128x160+ST7735  
     2,2" Display 320x240 ILI9341 9-pin (JB8) - https://www.ebay.de/sch/i.html?_nkw=2.2+ILI9341+240x320  
 
 
