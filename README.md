# Observatory Build

## Description

## Table of Contents
* [Hardware](#hardware)
* [Eagle Software Load](#eagle-software-load)
* [Re-Imaging the Eagle Computer](#re-imaging-the-eagle-computer)
* [Software Updates](#software-updates)
* [Required Software](#required-software)
* [COM Port Assignment](#com-port-assignment)
* [Drive Mapping](#drive-mapping)

## Hardware

| Component | Manufacturer          |
| --------- | ----------------------|
| Telescope | SkyWatcher Esprit 120 |
| Camera | ZWO ASI071MC Pro |
| Guider | WO Off Axis Guider |
| Guide Camera | ZWO ASI174MM |
| Filter Holder | ZWO M42 Filter Holder |
| Computer | Prima Luce Lab Eagle 4 |
| Focuser | Prima Luce Lab 3" ESATTO |
| Rotator | Prima Luce Lab 3" ARCO |
| Flat Panel | Prima Luce Lab GIOTTO 185 |
| Cover Motor | Prima Luce Lab ALTO-1 |
| Mount | iOptron CEM70G Mount |
| Pier | Astroworx 800mm Pier |
| Observatory | NexDome 2.2m Dome |
| Weather Station | AAG CloudWatcher Cloud Detector and Solo Computer |



## Eagle Software Load

1. ASCOM 6 Platform
2. iOptron CEM70 Driver
3. ZWO ASI071MC Pro Driver
4. ZWO ASI174MM Driver
5. Eagle X
6. NexDome Drivers
7. ESATTO Driver
8. ARCO Driver
9. ECCO Driver
10. GIOTTO Driver
11. ALTO Driver
12. PHD2 Software
13. Cartes du Ciel
14. NINA

## Re-Imaging the Eagle Computer

The Eagle Computer can be restored to its original state by restoring the Macrium Reflect Image backup.

This process requires the Rescue PE disk and the IMage disk.

1. Place Rescue PE Disk in USB Drive
2. Place Image Disk in USB Drive
3. Reboot PC & Press F10
4. Select USB Boot Loader
5. Image Restore - Browse for Image File
6. Select Image Drive & select image file ...00-00.mrimg & click OK
7. Select Restore Image
8. Confirm Destination  & Click Next
9. Click Finish

The original Eagle Image will be restored.

Remove the USB Disks & reboot. Windows will reboot and download necesssary updates.

## Software Updates

1. Update ASCOM - 6.5 -> 6.6
2. Eagle Manager - 4.2
3. Update PHD2
4. Update location in Cartes du Ciel

## Required Software 

1. iOptron CEM70 - iOptron Commander and ASCOM Driver
2. ZWO Camera Driver - ASI071MCPro and ASI174MM
3. NINA
4. ECCO
5. PLL ASCOM Switch
6. ESATTO
7. ARCO
9. ALTO
7. NexDome
8. ASTAP and D50 Stars Database
9. Lunatico Cloudwatcher Safety Monitor

## COM Port Assignment

1. ESATTO - Silicon Labs CP210x USB to UART Bridge (COM8)
2. ARCO - Silicon Labs CP210x USB to UART Bridge (COM8)
3. GIOTTO - Silicon Labs CP210x USB to UART Bridge (COM9)
4. ALTO - Silicon Labs CP210x USB to UART Bridge (COM10)
5. NexDome - Silicon Labs CP210x USB to UART Bridge (COM12)

## Drive Mapping

1. AAGSOLO ( \\\\10.0.0.14) (Y:)
2. Eagle Session ( \\\\deep-thought ) (Z:)




