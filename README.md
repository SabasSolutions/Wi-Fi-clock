# Wi-Fi-clock
Desktop Wi-Fi clock made from old Tetris, esp32c6, st7735. There are functions of online time synchronization, photo frames, logo demonstration and analogue of the magic ball from the movie Route 60.

[Video on YouTube](https://www.youtube.com/shorts/ss9aqswdIiM)

### Components needed for assembly:
1. ESP32C6 QFN32 (WeActStudio)
2. WeActStudio ST7735 128x160 RGB Display
3. Tetris case
4. Wires 30AWG
5. USB Cable

### Libraries required:
1. NTPClient from Fabrice Weinberg
2. Adafruit-GFX-Library
3. Adafruit-ST7735-Library

![Clock](/images/coputer1.jpg)

> [!IMPORTANT]
> The board pins for connecting to the display and buttons can be manually assigned via code, but some pins are responsible for other board features, so it is better not to use them. For connecting the display, the best GPIOs are 2,4,5,6,7 according to Table 2-11.

![Table 2-11](/images/table.png)
![IO MUX](/images/spi.png)

> [!IMPORTANT]
> For the display to work correctly, it is necessary to make changes to the Adafruit_ST7735.cpp file of the Adafruit_ST7735_and_ST7789_Library library. After line 232 you need to add: 
_colstart = 2;
_rowstart = 1;
> The final view should be like this:

![Adafruit_ST7735.cpp](/images/Adafruit_ST7735cpp.png)
