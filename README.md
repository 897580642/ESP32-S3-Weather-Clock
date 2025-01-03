# ESP32-S3-Weather-Clock
ESP32-S3 Weather Clock based on LVGL （Arduino）.


Ardunio （PlatformIO）:
PLATFORM: Espressif 32 (6.5.0) > Espressif ESP32-S3-DevKitC-1-N8 (8 MB QD, No PSRAM)
HARDWARE: ESP32S3 240MHz, 320KB RAM, 8MB Flash
DEBUG: Current (esp-builtin) On-board (esp-builtin) External (cmsis-dap, esp-bridge, esp-prog, iot-bus-jtag, jlink, minimodule, olimex-arm-usb-ocd, olimex-arm-usb-ocd-h, olimex-arm-usb-tiny-h, olimex-jtag-tiny, tumpa)
PACKAGES:
 - framework-arduinoespressif32 @ 3.20014.231204 (2.0.14)
 - tool-esptoolpy @ 1.40501.0 (4.5.1)
 - toolchain-riscv32-esp @ 8.4.0+2021r2-patch5
 - toolchain-xtensa-esp32s3 @ 8.4.0+2021r2-patch5
  
 
Note：

Espressif 32版本不要选的太高，不兼容的话烧写进去会无限重启...

基于LVGL （Arduino）

硬件：ESP32S3 + LCD（ILI9341 SPI屏）

支持心知天气和和风天气获取天气数据（需要自己申请账号），支持WIFI配网（）

 /* 和风天气 - https://dev.heweather.com */

HEFENG_KEY = "";//和风天气秘钥,替换成自己的秘钥


HEFENG_LOCATION = "101280306";//城市ID,可到https://where.heweather.com/index.html查询,替换成自己的城市ID

/* 心知天气 - https://www.seniverse.com */

SENIVERSE_KEY = "";//心知天气秘钥,替换成自己的秘钥

SENIVERSE_LOCATION = "Huicheng";//城市列表 https://docs.seniverse.com/api/start/start.html,替换成自己的城市名称

硬件接线：
Location:   .pio/libdeps/esp32-s3/TFT_eSPI/User_Setup.h
vcc接3.3v,GND接GND，LED接5v/3.3v就完成了，一共连接8个PIN脚 （暂未实现触屏效果）

WIFI配置：
src/main.cpp里wifiManager.autoConnect("","")里添加wifi名字和密码

成果展示:
![image](doc/PictureShow/20250103205747.jpg)
![image](doc/PictureShow/20250103205819.jpg)

