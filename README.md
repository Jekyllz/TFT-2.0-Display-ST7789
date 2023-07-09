### TFT-2.0-Display-ST7789
How to drive a TFT Screen using CS Pin with ST7789 driver

TFT Display 0.96 1.3 1.14 1.54 2.0 Inch IPS 7P SPI HD 65K Color LCD Module ST7735

##Parts Used
2.0Inch screen here [Ali.Express.tft.screen]([url](https://nl.aliexpress.com/item/32859772356.html?spm=a2g0o.order_list.order_list_main.401.df0379d2loXv5B&gatewayAdapt=glo2nld)https://nl.aliexpress.com/item/32859772356.html?spm=a2g0o.order_list.order_list_main.401.df0379d2loXv5B&gatewayAdapt=glo2nld)
Arduino Nano (mines a clone)
18650 BMS I use a customised tp4056 that provides adjustable output [Ali.express.tp4056.output]([url](https://nl.aliexpress.com/item/1005004616088520.html?spm=a2g0o.order_list.order_list_main.108.21ef79d2kQJoub&gatewayAdapt=glo2nld)https://nl.aliexpress.com/item/1005004616088520.html?spm=a2g0o.order_list.order_list_main.108.21ef79d2kQJoub&gatewayAdapt=glo2nld)
18650 Battery & 18650 battery holder (easy to google and find)

##Wiring
BLK - Not Used
TFT_RST 9 // (RS, RES) reset pin
TFT_MOSI 11 (SDA)
TFT_SCLK 13 (Referred to as CLK, SCL, SLCK, It's not I2C Don't be deceived)
TFT_CS 10 // if your display has CS pin
TFT_DC 8 // data pin
VCC = // Postive Power 3v3 Only! (5v will destroy)
GND = Ground, Negative.

![tft-screen-pin-layout](https://github.com/Jekyllz/TFT-2.0-Display-ST7789/assets/24834166/2b9ab6d6-14ef-467c-a98e-e7d440d3734c)


##Arduino Libraries
Open the Library Manager:
In the menu bar, select Tools > Manage Libraries…
In IDE 2, you can also click on the Library Manager icon button in the sidebar.
Find the library in the search results. The results are listed alphabetically, so you may need to scroll down the list.
Find a library you want to install. You can review the description and author. When you’ve found a library you want to install, click Install. The latest version is selected by default.

##Install these Libraries:
  Adafruit_GFX.h    // Core graphics library
  Adafruit_ST7789.h // Hardware-specific library for ST7789

##Download .ino and upload to arduino :)


Credit to limchengwei in the original Code for Arduino Mega that has been ammended [arduino mega]([url](https://www.hackster.io/limchengwei/st7789-lcd-with-arduino-mega-and-potential-divider-3db631)https://www.hackster.io/limchengwei/st7789-lcd-with-arduino-mega-and-potential-divider-3db631)


