### TFT-2.0-Display-ST7789
How to drive a TFT Screen using CS Pin with ST7789 driver

TFT Display 0.96 1.3 1.14 1.54 2.0 Inch IPS 7P SPI HD 65K Color LCD Module ST7735

![tft-screen-pin-layout](https://github.com/Jekyllz/TFT-2.0-Display-ST7789/assets/24834166/2b9ab6d6-14ef-467c-a98e-e7d440d3734c)


## Parts Used
* 2.0Inch screen here [Ali.Express.tft.2.0.screen](https://nl.aliexpress.com/item/32859772356.html?spm=a2g0o.order_list.order_list_main.401.df0379d2loXv5B&gatewayAdapt=glo2nld)
* Arduino Nano (mines a clone) [Arduino Nano](https://www.amazon.co.uk/gp/product/B072BMYZ18/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
* 18650 BMS I use a customised tp4056 that provides adjustable output [Ali.express.tp4056.bms](https://nl.aliexpress.com/item/1005004616088520.html?spm=a2g0o.order_list.order_list_main.108.21ef79d2kQJoub&gatewayAdapt=glo2nld)
  
* 18650 Battery & 18650 battery holder (easy to google and find) [Holder](https://nl.aliexpress.com/item/1005005084346241.html?spm=a2g0o.productlist.main.3.4efc75886lWDEn&algo_pvid=a93a391b-e36f-4ed0-99de-d28d16f3f60e&algo_exp_id=a93a391b-e36f-4ed0-99de-d28d16f3f60e-1&pdp_npi=3%40dis%21GBP%215.83%212.8%212.62%21%217.21%21%21%4021227f0f16889136359864900d077a%2112000031584753183%21sea%21UK%212497487056&curPageLogUid=K0xFXddcbtTP) ; [Battery](https://nl.aliexpress.com/item/32810252344.html?spm=a2g0o.order_list.order_list_main.81.21ef79d2BWutpn&gatewayAdapt=glo2nld)

  
## Wiring
* BLK - Not Used
* TFT_RST 9 // (RS, RES) reset pin
* TFT_MOSI 11 (SDA)
* TFT_SCLK 13 (Referred to as CLK, SCL, SLCK, It's not I2C Don't be deceived)
* TFT_CS 10 // if your display has CS pin
* TFT_DC 8 // data pin
* VCC = // Postive Power 3v3 Only! (5v will destroy)
* GND = Ground, Negative.


## Arduino Libraries
In Arduino IDE - Open the Library Manager:
* In the menu bar, select Tools > Manage Libraries…
In IDE 2, you can also click on the Library Manager icon button in the sidebar.
Find the library in the search results. The results are listed alphabetically, so you may need to scroll down the list.
Find a library you want to install. You can review the description and author. When you’ve found a library you want to install, click Install. The latest version is selected by default.

## Install these Libraries:
* Adafruit_GFX.h    // Core graphics library
* Adafruit_ST7789.h // Hardware-specific library for ST7789

Download .ino on this Repository and upload with Arduino IDE :)

The code can further be adjusted
Notice at line 20 init. the width and space of the screen
```
tft.init(240, 320, SPI_MODE3);           // Init ST7789 240x320
```
Or rotation of dislay
```
tft.setRotation(2)
```
SPI Speed Frequency:
```
tft.setSPISpeed(40000000);
```

Credit to limchengwei in the original Code for Arduino Mega that has been ammended for use wtih the arduino Nano. [arduino mega](https://www.hackster.io/limchengwei/st7789-lcd-with-arduino-mega-and-potential-divider-3db631)


