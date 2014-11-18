Netduino HY-1.8 SPI TFT Driver
==============================

Netduino library for the HY 1.8 SPI TFT Display based on an older Adafruit ST7735 library.

This display, which is *extremely* similar to the AdaFruit ST7735, is frequently found on ebay and is a great 1.8 inch SPI TFT display.

I have pin out and wiring details in my [blog post](http://www.stefangordon.com/driving-the-hy-1-8-spi-tft-128x160-display-from-a-netduino/).

Usage is pretty simple – here is an example using the pin assignments I listed above:
```csharp
var lcd = new HY18SPI(Pins.GPIO_PIN_D9, Pins.GPIO_PIN_D7, Pins.GPIO_PIN_D8, SPI.SPI_module.SPI1, 15000);
lcd.AutoRefreshScreen = true;
lcd.ClearScreen((ushort)HY18SPI.Colors.White);
lcd.DrawCircle(10, 10, 20, (ushort)HY18SPI.Colors.Red);</pre>
```

This is all based on the existing Netduino Helpers library for the AdaFruit ST7735.
