# VIEWEDISPLAY
My attempts at making VIEWE DISPLAY 5.0 inch work with esp-32-display-panel library

![image](https://github.com/user-attachments/assets/5a9e9b75-b743-484a-be3c-21aad97f1e7f)

I am using the configuration files in this git, all the pins should be corrected for my display

pins taken from this https://github.com/VIEWESMART/ESP32-Arduino/blob/31ba5a6dca7e777f4b43b76368286532fe487b7c/examples/7.0inch/Libraries/ESP32_Display_Panel/src/board/viewe/ESP_viewe_panel_8048070.h 
and
https://docs.google.com/viewer?url=https%3A%2F%2Fviewedisplay.com%2Fwp-admin%2Fadmin-ajax.php%3Fjuwpfisadmin%3Dfalse%26action%3Dwpfd%26task%3Dfile.download%26wpfd_category_id%3D73%26wpfd_file_id%3D6346%26token%3D%26preview%3D1&embedded=true
to double check

using LVGL 8.4, esp32-display-panel 0.1.8, esp32_io_expander 0.0.4

error at serial

17:12:44.615 -> LVGL rotation example start
17:12:44.615 -> Initialize panel device
17:12:44.615 -> Initialize LVGL
17:12:44.615 -> Create UI
17:12:44.615 -> Guru Meditation Error: Core  1 panic'ed (LoadProhibited). Exception was unhandled.
17:12:44.647 -> 
17:12:44.647 -> Core  1 register dump:
17:12:44.647 -> PC      : 0x42007b3b  PS      : 0x00060230  A0      : 0x820070a1  A1      : 0x3fcebcc0  
17:12:44.679 -> A2      : 0x00000000  A3      : 0x0000003c  A4      : 0x00000009  A5      : 0x0000ff00  
17:12:44.679 -> A6      : 0x00ff0000  A7      : 0xff000000  A8      : 0x8201f182  A9      : 0x3fcebca0  
17:12:44.679 -> A10     : 0x3fcecb68  A11     : 0x00000000  A12     : 0x00000004  A13     : 0x3fcecba4  
17:12:44.679 -> A14     : 0x00ff0000  A15     : 0x00000000  SAR     : 0x0000001f  EXCCAUSE: 0x0000001c  
17:12:44.722 -> EXCVADDR: 0x00000022  LBEG    : 0x400570e8  LEND    : 0x400570f3  LCOUNT  : 0xffffffff  
17:12:44.722 -> 
17:12:44.722 -> 
17:12:44.722 -> Backtrace: 0x42007b38:0x3fcebcc0 0x4200709e:0x3fcebce0 0x4202422f:0x3fcebd00 0x42002372:0x3fcebd20 0x4202a65e:0x3fcebd80 0x4037dd2e:0x3fcebda0
17:12:44.722 -> 
17:12:44.722 -> 
17:12:44.722 -> 
17:12:44.722 -> 
17:12:44.722 -> ELF file SHA256: a5081b528bd58f92
17:12:44.722 -> 
17:12:44.976 -> Rebooting...
17:12:44.976 -> �ESP-ROM:esp32s3-20210327
17:12:44.976 -> Build:Mar 27 2021
17:12:44.976 -> rst:0xc (RTC_SW_CPU_RST),boot:0x8 (SPI_FAST_FLASH_BOOT)
17:12:44.977 -> Saved PC:0x403791ce
17:12:44.977 -> SPIWP:0xee
17:12:44.977 -> mode:DIO, clock div:1
17:12:44.977 -> load:0x3fce3818,len:0x109c
17:12:44.977 -> load:0x403c9700,len:0x4
17:12:45.021 -> load:0x403c9704,len:0xb50
17:12:45.021 -> load:0x403cc700,len:0x2fe4
17:12:45.021 -> entry 0x403c98ac

on loop
