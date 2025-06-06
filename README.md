# M0_Digital_Eyes
Project files for digital eyes using AdaFruit ItsyBitsy M0 Express

## Code by AdaFruit
Not my original code- copied from AdaFruit.

I made the AdaFruit Eyes project with a Raspberry Pi and the Eyes Bonnet, which worked great, but I found the full sized Pi too bulky to cram into a skull. 
Later I came across the UncannyEyes project (https://github.com/adafruit/Uncanny_Eyes) using an ItsyBitsy board- much smaller and cheaper, with on board memory and low power draw. There is also virtually no boot up time, and the performance was way better than the Pi Zero. 

This repository is mostly for my own reference when doing any maintenance on these or expirimenting with other displays. 

Adafruit ItsyBitsy M0 - https://www.adafruit.com/product/3727
![adafruit_ItsyBitsy_M0](https://github.com/user-attachments/assets/c73cabf8-3e75-424f-a60c-52ac239142f0)



## Lenses
Optical glass lenses
![image](https://github.com/user-attachments/assets/09595f77-a3d1-419a-85fd-2bfa66164d87)  
OD = 40mm  
ID = 36  
H = 16  
E = 2.5  
https://www.aliexpress.us/item/3256804130163482.html  

## Wiring
**ItsyBitsy  ---->   LCD**  
G  ---->   GND  
USB  ---->   VCC  
10  ---->   CS (Right Eye)  
9  ---->   CS (Left Eye)  
7  ---->   AO  
RST  ---->   RESET  
SCK  ---->   SCK  
MOSI  ---->   SDA  

On the LCD
VCC---68Ω resistor---> LED- Remove the SMD resistor on the trace and solder the resistor to the lower solder pad. 
There IS a 3.3V pin on the board that may work on the LED pin, which would require another wire. I haven't tried it yet.  

![image](https://github.com/user-attachments/assets/f27f43d1-415f-4987-a127-c3050e23ebf7)  

## Code
Arduino IDE - add additional boards to preferences: https://learn.adafruit.com/introducing-itsy-bitsy-m0/setup  
Code homepage: https://learn.adafruit.com/animated-electronic-eyes/software  

"Double click" reset button on board to enter bootloader mode (small red LED pulsing) to upload sketch. MAy beed to select new port on IDE.  


