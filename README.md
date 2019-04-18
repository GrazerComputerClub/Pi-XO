# Pi-XO
Raspberry Pi Zero game console for use with PICO-8 

The hardware and software is sill under development. 
Rev. 01. board  error:
  - speaker connected to GND (do not wire speaker to PCB), please connect speaker to audio amp. output via wire.
  - ADC input direct connected to batterie A result in applying voltage to 3.3v supply if batterie is attached - do not wire ADC IC 

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
 1 x Switch 3 Pin (S9)
 8 x Tactile switch 6x6mm (S1-S7)  
 1 x Audio amplifier board PAM8302 (JP3, do not connect PAD5 and PAD6)
 1 x Speaker 8 Ohm (connect to amplifier board PAM8302 Output via wire)
 1 x LED bar 8 components (right site)
 1 x Resistor array 1K (RN1) 
 2 x Vibration motor (JP4, JP5)
 
 
 
