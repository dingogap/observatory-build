# Observatory Build

## Description

## Table of Contents
1. [Hardware](#hardware)
2. [Eagle Software Load](#eagle-software-load)
3. [Re-Imaging the Eagle Computer](#re-imaging-the-eagle-computer)
4. [Software Updates](#software-updates)
5. [Required Software](#required-software)
6. [WiFi Connections](#wifi-connections)
7. [COM Port Assignment](#com-port-assignment)
8. [Drive Mapping](#drive-mapping)
9. [Installation Checklist](#installation-checklist)
10. [NINA Configuration](#nina-configuration)
11. [NexDome Configuration](#nexdome-configuration)
12. [Windows Update Settings](#windows-update-settings)

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
15. Lunatico Cloudwatcher Safety Monitor

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
5. PLL ASCOM Switch (in the Manger 4.2 folder)
6. ESATTO
7. ARCO
9. ALTO
7. NexDome
8. ASTAP and D50 Stars Database
9. Lunatico Cloudwatcher Safety Monitor

## WiFi Connections
The Observatory uses WiFi for as many devices as possible delivered by a WiFi5 Router connected by ethernet to the main network.


| Device | IP Address | Subnet Mask | Gateway|
|--------|------------|------|-
| Router | 10.0.0.30 | 255.255.255.0 |10.0.0.1
| Eagle 4 Computer | 10.0.0.31 | 255.255.255.0 |10.0.0.30 
| NexDome Observatory| 10.0.0.32 | 255.255.255.0 |10.0.0.30
| CEM70G Mount | 10.0.0.33 | 255.255.255.0 | 10.0.0.30



## COM Port Assignment

1. ESATTO - Silicon Labs CP210x USB to UART Bridge (COM7)
2. ARCO - Silicon Labs CP210x USB to UART Bridge (COM7)
3. GIOTTO - Silicon Labs CP210x USB to UART Bridge (COM11)
4. ALTO - Silicon Labs CP210x USB to UART Bridge (COM10)

## Drive Mapping

1. AAGSOLO ( \\\\10.0.0.14) (Y:)
2. Eagle Session ( \\\\betelgeuse ) (Z:)

## Installation Checklist
- [ ] ASCOM 6 Platform
- [ ] iOptron CEM70 Driver
- [ ] ZWO ASI071MC Pro Driver
- [ ] ZWO ASI174MM Driver
- [ ] Eagle X?
- [ ] NexDome Drivers
- [ ] ESATTO Driver
- [ ] ARCO Driver
- [ ] ECCO Driver
- [ ] GIOTTO Driver
- [ ] ALTO Driver
- [ ] PHD2 Software
- [ ] Cartes du Ciel
- [ ] NINA
- [ ] WiFi Configuration
- [ ] Lunatico CloudWatcher Safety Monitor

## NINA Configuration

### Equipment

#### 1. Camera
  Camera - ZWO 071MC Pro
   * Dew Heater: On
   * Cooling to -10°C 
     * duration 15 minutes
   * Warming
     * duration 5 minutes

#### 2. Filter Wheel
   * NINA Manual Filer Wheel

#### 3. Focuser
   * PLL Ascom Focuser
     * Com Port 7
     * Dark Mode On

#### 4. Rotator
   * PLL Ascom Rotator
      * Com Port 7

#### 5. Telescope 
   * iOptron CEM70G
      * Connection: WiFi

#### 6. Guider
   * Application: PHD2
   * Guide Camera: ZWO ASI 174MM
   * Method: Off Axis Guiding

#### 7. Flat Panel
   * Driver: PLL Cover Calibrator
   * Cover Motor - PLL Alto
      * Com Port 10
   * Flat Panel: PLL Giotto
      * Com Port 11

#### 8. Weather
   * Lunatico CloudWatcher Observing Conditions
   * AAGSOLO ( \\\\10.0.0.14) mapped as Drive Y:
   * Path:  Y:\aag_json.dat

#### 10. Dome
   * Beaver NexDome ASCOM Driver
   * Connection From Telescope: IP
      * Address: 10.0.0.32
      * Port: 10000

#### 11. Safety Monitor
   * Lunatico CloudWatcher Safety Monitor


### Options

#### 1. General
   * Name: Observatory
   * Astrometry: C:\Users\PrimaLuceLab\Documents\N.I.N.A\dome-horizon.hrz

#### 2. Equipment
   * Camera:

   * Telescope:
      * Name :Skywatcher Esprit 120
      * Focal Length: 840mm
      * Focal Ration: 7
      * Settle After Slew: 7s

   * Weather

   * Filter Wheel

   * Planetarium

#### 3. Autofocus

#### 4. Dome

   * Dome & Mount Geometry

      | Item| Setting|
      |-----|---------
      |Mount Type| Equatorial|
      | Telescope Position N/S| 22mm|
      |Telescope Position E/W |-9mm|
      |Telescope Position +Up/-Down| -325mm|
      |Dome Radius| 1100mm|
      |GEM Axis Length|300mm|
      |Lateral Axis Length| 0mm|
      |Azimuth Tolerance| 2° |
    
   * Dome Settings        

      |Item| Setting|
      |----|--------|
      |Synchronisation Timeout|120s|
      |Settle After Slew| 10s|
      |Allow Sync While Mount Slews| Off|
      |Sync slew Dome when scope slews|On|
      |Find Home before Parking|Off|

#### 5. Imaging

## Nexdome Configuration

### 1. Beaver Dome Test And Config

   * Configure Wifi (Client)

      |Item| Setting|
      |----|--------|
      |Client|Active|
      |SSID|Wifi NetWork Name|
      |IP Type|Static|
      |IP Address| 10.0.0.32|
      |Subnet Mask| 255.255.255.0|
      |Gateway| 10.0.0.30|
      | Listen port| 10000|

   * Motor Details

      |Item| Setting|
      |----|--------|
      |Steps/Degree|152.988889|
      |Min Speed|400|
      |Max Speed|800|
      |Acceleration|400|
      |Size of Home Sensor|2.000000|
      |Location of Home Sensor|180|

   * Configuration
      
      |Item| Setting |
      |----|---------|
      |IP Address|10.0.0.32|
      |Port|10000|
      |Home Azimuth|180°|
      |Park Azimuth|180°|

  * Safety Settings

      |Item| Setting |
      |----|---------|
      |Shutter Battery| checked |
      |Min Voltage| 11.0 | 

## Windows Update Settings

#### 1. Active Hours

Windows will automatically reboot the PC if an update has been applied. An Active Hourse Excluion can be set to stop the PC rebooting during an imaging session.

**Change the Active Hours to:**
* Start Time: 6:00 pm
* End Time: 8:00 am








