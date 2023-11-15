# Wi-Fi SoftAP Example

(See the README.md file in the upper level 'examples' directory for more information about examples.)

This example shows how to use the Wi-Fi SoftAP functionality of the Wi-Fi driver of ESP for serving as an Access Point.

## How to use example

### Configure the project

Open the project configuration menu (`idf.py menuconfig`). 

In the `Example Configuration` menu:

* Set the Wi-Fi configuration.
    * Set `WiFi SSID`.
    * Set `WiFi Password`.

Optional: If you need, change the other options according to your requirements.

### Build and Flash

Build the project and flash it to the board, then run the monitor tool to view the serial output:

Run `idf.py -p PORT flash monitor` to build, flash and monitor the project.

(To exit the serial monitor, type ``Ctrl-]``.)

See the Getting Started Guide for all the steps to configure and use the ESP-IDF to build projects.

* [ESP-IDF Getting Started Guide on ESP32](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/index.html)
* [ESP-IDF Getting Started Guide on ESP32-S2](https://docs.espressif.com/projects/esp-idf/en/latest/esp32s2/get-started/index.html)
* [ESP-IDF Getting Started Guide on ESP32-C3](https://docs.espressif.com/projects/esp-idf/en/latest/esp32c3/get-started/index.html)

## Example Output

There is the console output for this example:

```
I (917) phy: phy_version: 3960, 5211945, Jul 18 2018, 10:40:07, 0, 0
I (917) wifi: mode : softAP (30:ae:a4:80:45:69)
I (917) wifi softAP: wifi_init_softap finished.SSID:myssid password:mypassword
I (26457) wifi: n:1 0, o:1 0, ap:1 1, sta:255 255, prof:1
I (26457) wifi: station: 70:ef:00:43:96:67 join, AID=1, bg, 20
I (26467) wifi softAP: station:70:ef:00:43:96:67 join, AID=1
I (27657) tcpip_adapter: softAP assign IP to station,IP is: 192.168.4.2
```

## Troubleshooting

For any technical queries, please open an [issue](https://github.com/espressif/esp-idf/issues) on GitHub. We will get back to you soon.



```
entry 0x40080698
I (29) boot: ESP-IDF v4.4.4-dirty 2nd stage bootloader
I (29) boot: compile time 12:12:37
I (29) boot: chip revision: v3.0
I (33) boot_comm: chip revision: 3, min. bootloader chip revision: 0
I (40) boot.esp32: SPI Speed      : 40MHz
I (44) boot.esp32: SPI Mode       : DIO
I (49) boot.esp32: SPI Flash Size : 2MB
I (54) boot: Enabling RNG early entropy source...
I (59) boot: Partition Table:
I (62) boot: ## Label            Usage          Type ST Offset   Length
I (70) boot:  0 nvs              WiFi data        01 02 00009000 00006000
I (77) boot:  1 phy_init         RF data          01 01 0000f000 00001000
I (85) boot:  2 factory          factory app      00 00 00010000 00100000
I (92) boot: End of partition table
I (96) boot_comm: chip revision: 3, min. application chip revision: 0
I (103) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=12c54h ( 76884) map
I (140) esp_image: segment 1: paddr=00022c7c vaddr=3ffb0000 size=0389ch ( 14492) load
I (146) esp_image: segment 2: paddr=00026520 vaddr=40080000 size=09af8h ( 39672) load
I (162) esp_image: segment 3: paddr=00030020 vaddr=400d0020 size=6f104h (454916) map
I (327) esp_image: segment 4: paddr=0009f12c vaddr=40089af8 size=0b13ch ( 45372) load
I (356) boot: Loaded app from partition at offset 0x10000
I (356) boot: Disabling RNG early entropy source...
I (368) cpu_start: Pro cpu up.
I (368) cpu_start: Starting app cpu, entry point is 0x400811c4
0x400811c4: call_start_cpu1 at C:/Espressif/frameworks/esp-idf-v4.4.4/components/esp_system/port/cpu_start.c:148

I (0) cpu_start: App cpu up.
I (382) cpu_start: Pro cpu start user code
I (382) cpu_start: cpu freq: 160000000
I (382) cpu_start: Application information:
I (387) cpu_start: Project name:     wifi_softAP
I (392) cpu_start: App version:      1
I (396) cpu_start: Compile time:     Nov 15 2023 12:12:04
I (403) cpu_start: ELF file SHA256:  33d18cff210dbb0f...
I (409) cpu_start: ESP-IDF:          v4.4.4-dirty
I (414) heap_init: Initializing. RAM available for dynamic allocation:
I (421) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (427) heap_init: At 3FFB7270 len 00028D90 (163 KiB): DRAM
I (433) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (440) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (446) heap_init: At 40094C34 len 0000B3CC (44 KiB): IRAM
I (454) spi_flash: detected chip: generic
I (457) spi_flash: flash io: dio
W (461) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (475) cpu_start: Starting scheduler on PRO CPU.
I (0) cpu_start: Starting scheduler on APP CPU.
I (561) wifi softAP: ESP_WIFI_MODE_AP
I (571) wifi:wifi driver task: 3ffbf8c4, prio:23, stack:6656, core=0
I (571) system_api: Base MAC address is not set
I (571) system_api: read default base MAC address from EFUSE
I (591) wifi:wifi firmware version: 6567a16
I (591) wifi:wifi certification version: v7.0
I (591) wifi:config NVS flash: enabled
I (591) wifi:config nano formating: disabled
I (601) wifi:Init data frame dynamic rx buffer num: 32
I (601) wifi:Init management frame dynamic rx buffer num: 32
I (611) wifi:Init management short buffer num: 32
I (611) wifi:Init dynamic tx buffer num: 32
I (611) wifi:Init static rx buffer size: 1600
I (621) wifi:Init static rx buffer num: 10
I (621) wifi:Init dynamic rx buffer num: 32
I (631) wifi_init: rx ba win: 6
I (631) wifi_init: tcpip mbox: 32
I (631) wifi_init: udp mbox: 6
I (641) wifi_init: tcp mbox: 6
I (641) wifi_init: tcp tx win: 5744
I (651) wifi_init: tcp rx win: 5744
I (651) wifi_init: tcp mss: 1440
I (651) wifi_init: WiFi IRAM OP enabled
I (661) wifi_init: WiFi RX IRAM OP enabled
I (671) phy_init: phy_version 4670,719f9f6,Feb 18 2021,17:07:07
I (761) wifi:mode : softAP (94:b5:55:f8:2d:6d)
I (771) wifi:Total power save buffer number: 16
I (771) wifi:Init max length of beacon: 752/752
I (771) wifi:Init max length of beacon: 752/752
I (771) wifi softAP: wifi_init_softap finished. SSID:SSID-192 password:123456789 channel:1
I (186311) wifi:new:<1,1>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (186311) wifi:station: c0:3c:59:85:f7:f0 join, AID=1, bgn, 40U
I (186341) wifi softAP: station c0:3c:59:85:f7:f0 join, AID=1
I (186471) esp_netif_lwip: DHCP server assigned IP to a station, IP is: 192.168.4.2
I (186611) wifi:<ba-add>idx:2 (ifx:1, c0:3c:59:85:f7:f0), tid:0, ssn:21, winSize:64
I (245281) wifi:station: c0:3c:59:85:f7:f0 leave, AID = 1, bss_flags is 658531, bss:0x3ffb8f80
I (245281) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (245291) wifi:<ba-del>idx
I (245291) wifi softAP: station c0:3c:59:85:f7:f0 leave, AID=1
```

![Screenshot 2023-11-15 121353](https://github.com/Siracha192/ESP32_ESP-IDF_WiFi-AP-Sent/assets/115066298/3598befd-faec-4ea8-86b0-6371fa0c0e39)

![Screenshot 2023-11-15 122151](https://github.com/Siracha192/ESP32_ESP-IDF_WiFi-AP-Sent/assets/115066298/4b49d89c-5539-406c-8581-c3102ae2b524)

![Screenshot 2023-11-15 121734](https://github.com/Siracha192/ESP32_ESP-IDF_WiFi-AP-Sent/assets/115066298/472c0429-6c44-430a-8d8d-45b746a652ca)


