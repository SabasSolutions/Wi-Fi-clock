# Wi-Fi-clock
Desktop Wi-Fi clock made from old Tetris, esp32c6, st7735. There are functions of online time synchronization, photo frames, logo demonstration and analogue of the magic ball from the movie Route 60.

[Video on YouTube](https://www.youtube.com/shorts/ss9aqswdIiM)

### Components needed for assembly:
1. ESP32C6 QFN32 (WeActStudio)
2. WeActStudio ST7735 128x160 RGB Display
3. Tetris case
4. Wires 30AWG
5. USB Cable

![Clock](/images/coputer1.jpg)

> [!IMPORTANT]
> The board pins for connecting to the display and buttons can be manually assigned via code, but some pins are responsible for other board features, so it is better not to use them. For connecting the display, the best GPIOs are 2,4,5,6,7 according to Table 2-11.

![Table 2-11](/images/table.png)
![IO MUX](/images/spi.png)
