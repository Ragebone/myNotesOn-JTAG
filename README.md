# myNotesOn-JTAG

[Adafruit FT232H](https://www.adafruit.com/product/2264)
Using ith Openocd.
[Someones Thoughts and configs](https://forum.sparkfun.com/viewtopic.php?t=46655)
```
interface ftdi
ftdi_vid_pid 0x0403 0x6014
ftdi_layout_init 0x0008 0x400b
adapter_khz 1000
transport select jtag

#ftdi_device_desc "Adafruit FT232H Breakout"
#ftdi_serial "FTZ7O8O0"
#ftdi_layout_init 0x0018 0x05fb
```



selfbuilt copy pasted config 
```
#This configuration file is created for a tutorial: 
#”Getting Started with OPENOCD Using FT2232H Adapter for SWD Debugging”
#Written by:Yahya Tawil - yahya.tawil_at_gmail.com 
#Pulished on: http://www.allaboutcircuits.com 
#Version of OpenOCD:0.9.0
interface ftdi
transport select swd
ftdi_vid_pid 0x0403 0x6014
#ftdi_device_desc "USB Serial Converter A"
#ftdi_device_desc "FT2232H 开发板"
#ftdi_serial "FTZ7O8O0"
#adapter_khz 8
ftdi_layout_init 0x0018 0x05fb
ftdi_layout_signal SWD_EN -data 0
ftdi_layout_signal nSRST -data 0x0010

adapter speed 1000

```

it is from [this good tutorial](https://www.allaboutcircuits.com/technical-articles/getting-started-with-openocd-using-ft2232h-adapter-for-swd-debugging/)
that i need to continue with.

[SSDiag, stuff on SSDs](https://github.com/thesourcerer8/SSDdiag)
which laos links to the [The missing samsung evo repair manual](http://www2.futureware.at/~philipp/ssd/TheMissingManual.pdf)
[samsung firmware deobfuscation util](https://github.com/andy-knowles/samsung_ssd)
[another hrdware debugging tutorial on SSDs](https://wrongbaud.github.io/posts/jtag-hdd/)
[Harwarehacking JTAG tutorial](https://www.riverloopsecurity.com/blog/2021/07/hw-101-jtag-part3/)