/***************************************************
  This is a library for the Adafruit 1.8" SPI display.

This library works with the Adafruit 1.8" TFT Breakout w/SD card
  ----> http://www.adafruit.com/products/358
The 1.8" TFT shield
  ----> https://www.adafruit.com/product/802
The 1.44" TFT breakout
  ----> https://www.adafruit.com/product/2088
as well as Adafruit raw 1.8" TFT display
  ----> http://www.adafruit.com/products/618

  Check out the links above for our tutorials and wiring diagrams
  These displays use SPI to communicate, 4 or 5 pins are required to
  interface (RST is optional)
  Adafruit invests time and resources providing this open source code,
  please support Adafruit and open-source hardware by purchasing
  products from Adafruit!

  Written by Limor Fried/Ladyada for Adafruit Industries.
  MIT license, all text above must be included in any redistribution
 ****************************************************/

#include <Adafruit_GFX.h>    // Core graphics library
#include <Adafruit_ST7735.h> // Hardware-specific library
#include <SPI.h>


// For the breakout, you can use any 2 or 3 pins
// These pins will also work for the 1.8" TFT shield
#define TFT_RST    D0
#define TFT_CS     D1
#define TFT_DC     D2

// Option 1 (recommended): must use the hardware SPI pins
// (for UNO thats sclk = 13 and sid = 11) and pin 10 must be
// an output. This is much faster - also required if you want 
// to use the microSD card (see the image drawing example)
Adafruit_ST7735 tft = Adafruit_ST7735(TFT_CS,  TFT_DC, TFT_RST);

const uint16_t grey = 0x5AEB;
const uint16_t white = 0xFFFF;

void setup(void) {
  Serial.begin(115200);
  Serial.println();
  Serial.println("Hello! ST7735 TFT Test");

  tft.initR(INITR_BLACKTAB);   // initialize a ST7735S chip, black tab
  Serial.println("Initialized");
    
  tft.setTextWrap(false);
  tft.fillScreen(ST7735_BLACK);
  tft.setTextColor(grey);
  tft.setTextSize(2);
  tft.setCursor(10,10);
  tft.setRotation(tft.getRotation()+1);
  tft.println("!HOLA!");
  tft.setRotation(tft.getRotation()+1);
  tft.println("!HOLA!");
  tft.setRotation(tft.getRotation()+1);
  tft.println("!HOLA!");
  tft.setRotation(tft.getRotation()+1);
  tft.println("!HOLA!");
}

void loop() {

}
