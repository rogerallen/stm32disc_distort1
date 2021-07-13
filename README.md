# guitar distortion

Via https://www.youtube.com/watch?v=lNBrGOk0XzE
and https://www.youtube.com/watch?v=azLQf4aLv9w

# Adding I2S2

Started with default settings, then added I2S2 interface to connect to the Pmod Stereo interface

Mode & Configuration:
- Full Duplex master
- with Master Clock output

Parameter Settings
- Master Mode Transport
- I2S Philips
- 24 bits data on 32 bits frame (changed)
- 96 kHz (changed)

DMA Settings
- Add both TX & RX
- Circular FIFO
- I set to use Words, not Bytes since the frame is 32 bits.  He didn't show this.  :(

```
I/O    | Signal      | Pmod Pins
-------+-------------+------------------
PC6    | I2S2_MCK    | 7,  1 MCLK
PB12   | I2S2_WS     | 8,  2 LRCK
PB10   | I2S2_CK     | 9,  3 SCLK
PC2    | I2S2_ext_SD | 10    ADC SDOUT    
PC3    | I2S2_SD     |     4 DAC SDIN
GND    |             | 11, 5 GND
3.3V   |             | 12, 6 VCC
```