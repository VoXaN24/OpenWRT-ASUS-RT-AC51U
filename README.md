# OpenWRT-ASUS-RT-AC51U
---

## Installing OpenWRT on ASUS RT-AC51U

## Table of Contents
1. [Introduction](#introduction)
2. [Requirements](#requirements)
3. [Downloading OpenWRT Firmware](#downloading-openwrt-firmware)
4. [Flashing the Firmware](#flashing-the-firmware)
5. [Post-Installation Configuration](#post-installation-configuration)
6. [Reverting to Stock Firmware](#reverting-to-stock-firmware)
7. [Troubleshooting](#troubleshooting)

## Introduction
This guide will walk you through the process of installing OpenWRT on an ASUS RT-AC51U router. OpenWRT is a powerful, open-source router firmware that provides advanced networking features and customization options.

## Requirements
- ASUS RT-AC51U router
- Computer with Ethernet port
- Ethernet cable
- Internet connection
- Latest OpenWRT firmware for ASUS RT-AC51U
- A computer or VM with Windows 7 (11 is not supported by the ASUS Software)

## Downloading OpenWRT Firmware
1. Visit the [OpenWRT firmware download page](https://openwrt.org/toh/asus/rt-ac51u).
2. Download the latest stable release for the ASUS RT-AC51U. Look for a file named something like `openwrt-<version>-ramips-mt7620-rt-ac51u-squashfs-sysupgrade.bin` or use the file in the repo (last version 08/25).

## Flashing the Firmware
### Step 1: Connect to the Router
1. Connect your computer to the ASUS RT-AC51U router using an Ethernet cable. If you use a VM, set the network card to bridge
2. Set a static IP address on your computer. Use the following settings:
   - IP address: 192.168.1.2
   - Subnet mask: 255.255.255.0
   - Default gateway: 192.168.1.1

### Step 2: Access the Firmware Recovery Mode
1. Power off the router.
2. Press and hold the **Reset** button.
3. While holding the **Reset** button, power on the router. Continue holding the **Reset** button for about 10 seconds until the power LED starts flashing.

### Step 3: Flash the Firmware
1. Open a web browser on your computer and navigate to `http://192.168.1.1`.
2. The ASUS Firmware Restoration page should appear.
3. Click on **Browse** and select the downloaded OpenWRT firmware file.
4. Click **Upload** to start the firmware installation. The process may take several minutes. Do not power off or disconnect the router during this process.

### Step 4: Reboot the Router
1. Once the flashing process is complete, the router will automatically reboot.
2. Set your computer to obtain an IP address automatically (DHCP).

## Post-Installation Configuration
1. Connect to the router’s web interface by navigating to `http://192.168.1.1` in your web browser.
2. You should see the OpenWRT login page.
3. Set a new password for the router when prompted.
4. Configure the network settings according to your needs.

## Reverting to Stock Firmware
### Step 1: Download Stock Firmware
1. You can find the stock firmware file in the repo has ASUS has shutdown the page for it.

### Step 2: Flash Stock Firmware
1. Follow the same steps outlined in the **Flashing the Firmware** section, but use the stock firmware file instead of the OpenWRT firmware file.

## Troubleshooting
- **Router Not Responding**: Ensure all cables are securely connected and try resetting the router.
- **Unable to Access Web Interface**: Double-check your computer's IP settings and ensure it’s in the same subnet as the router (192.168.1.x).
- **Firmware Flashing Fails**: Make sure you are using the correct firmware file for the ASUS RT-AC51U.

For further assistance, visit the [OpenWRT forum](https://forum.openwrt.org/) or the [ASUS support page](https://www.asus.com/us/Networking/RTAC51U/HelpDesk/).

---

This guide should help you successfully install OpenWRT on your ASUS RT-AC51U router. Enjoy the enhanced capabilities and customization options that OpenWRT provides!
