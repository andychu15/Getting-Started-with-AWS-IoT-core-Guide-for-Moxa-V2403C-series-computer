# Getting Started with AWS IoT core Guide for Moxa V2403C series computer

# Document Information

## Revision History (Version, Date, Description of change)

| Version | Date        | Description of change |
| ------- | ----------- | --------------------- |
| 1       | 2022/02/15   | First release         |
|         |             |                       |

# Overview

The V2403C Series embedded computers are built around an Intel® Core™ i7/i5/i3 or Intel® Celeron® high-performance processor and come with up to 32 GB RAM, one mSATA slot, and two HDD/SSD for storage expansion. The computers are compliant with EN 50121-4, E1 mark, and ISO- 7637-2 standards making them ideal for rail-wayside and in-vehicle applications.

V2403C computers are equipped with a rich set of interfaces including 4 gigabit Ethernet ports, 4 RS-232/422/485 serial ports, 4 DIs, 4 DOs, and 4 USB 3.0 ports. In addition, they are also provided with 1 DisplayPort output and 1 HDMI output with 4K resolution.

Reliable connections and good power management are key to in-vehicle applications. The computers are provided with 2 mPCIe wireless expansion slots and 4 SIM-card slots to establish redundant LTE/Wi-Fi connectivity. In terms of power management, startup and shutdown delay mechanisms help in avoiding system malfunction and damage.

# Hardware Description

## DataSheet

[V2403C series](https://cdn-cms.azureedge.net/getmedia/2d3d196d-99b9-4f1b-817d-9c4f81dd3adf/moxa-v2403c-series-datasheet-v1.0.pdf)

## Standard Kit Contents

The standard shipping Moxa V2403C series computer package contains the following items:

- 1 x V2403C embedded computer
- 1 x Wall-mounting kit
- 1 x Storage disk tray package
- 1 x HDMI cable locker
- 1 x Quick installation guide (printed)
- 1 x Warranty card

## User Provided items

To setup and operate Moxa V2403C series computer, users have to prepare the following items by themselves.

- 10/100/1000M Ethernet cables
- Power adapter: input voltage 90 to 264 VAC, output voltage 24 V with 2.5 A DC load (can be purchased separately from Moxa)
- Power Cord: Power cord with AU/CN/EU/UK/US plug, 2.5A/250V, 1.83 m (can be purchased separately from Moxa)


Based on user’s application requirement, the following items are optional

- WiFi or Cellular module (can be purchased separately from Moxa)
- Antennas (can be purchased separately from Moxa)

## 3rd Party purchasable items
N/A

# Set up your Hardware Environment
- **Connecting a Display**

    Moxa V2403C series computer comes with HDMI interfaces on the rear panel. Connect a display monitor to the HDMI interfaces.

- **Connecting a Keyboard and Mouse**

    Connectors for a keyboard and mouse are located on the rear panel of the computer. Both connectors are USB interfaces; you can directly connect a keyboard and a mouse using these connectors.

- **Powering on Moxa V2403C series computer :**

	To power on the V2403C, connect the “terminal block to power jack converter” to the V2403C’s DC terminal block (located on the side panel),and then connect the 12 to 48 VDC power adapter. If the power is supplied properly, the Ready LED will glow a solid green after a 25 to 30 second delay. For surge protection, connect the grounding connector located below the power connector with the earth (ground) or a metal surface. 

- **Accessing Moxa V2403C series computer Using a Linux/Windows PC or Mac**

    You can use a PC to access Moxa V2403C series computer by using SSH over the network. Refer to the following IP addresses and login information:

    ![images/image2.png](images/image2.png)

    Login: moxa

    Password: moxa

    Root account login is disabled until you manually create a password for the account. The user moxa is in the sudo group so you can operate system level commands with this    user using the sudo command.

    **ATTENTION: For security reasons, we recommend that you disable the default user account and create your own user accounts or** 

    **Refer to Account Management of [Moxa V2403C series computer-linux-user-manual](https://cdn-cms.azureedge.net/getmedia/a116920c-a18a-428b-89b3-5ef9e3912309/moxa-v2403c-series-linux-manual-v1.0.pdf) for the detail steps.**

- **Change the network settings of Moxa V2403C series computer based on your network environment**

    Refer to the Changing the interfaces Configuration File of [Moxa V2403C series computer-linux-user-manual](https://cdn-cms.azureedge.net/getmedia/a116920c-a18a-428b-89b3-5ef9e3912309/moxa-v2403c-series-linux-manual-v1.0.pdf) for the detail steps.

# Set up your Development Environment

## Tools Installation (IDEs, Toolchains, SDKs)

The operation system of Moxa V2403C series is a native 64-bits X86 Linux operating system. There is no need to install toolchains. You can install development tools in Moxa V2403C series computer directly.

Follow these steps to update the package menu:

1. Make sure a network connection is available.

2. Use apt-get update to update the Debian package list.

```bash
moxa@Moxa:~$ sudo apt-get update
```

3. Install the native compiler and necessary packages.

```bash
moxa@Moxa:~$ sudo apt-get install gcc build-essential flex bison automake
```

# Setup your AWS account and Permissions

Refer to the instructions at [Set up your AWS Account](https://docs.aws.amazon.com/iot/latest/developerguide/setting-up.html). Follow the steps outlined in these sections to create your account and a user and get started:

- Sign up for an AWS account and
- Create a user and grant permissions.
- Open the AWS IoT console

Pay special attention to the Notes.

# Create Resources in AWS IoT

Refer to the instructions at [Create AWS IoT Resources](https://docs.aws.amazon.com/iot/latest/developerguide/create-iot-resources.html). Follow the steps outlined in these sections to provision resources for your Moxa V2403C series computer:

- Create an AWS IoT Policy
- Create a thing object

Pay special attention to the Notes.

> **Important**
Before you continue to the next step, your Moxa computer must be configured, and running. The Moxa computer must be connected to the Internet and you will need to be able to access the computer by using its command line interface. Command line access can be through SSH terminal remote interface.

# Build the demo

Follow above section, **Accessing Moxa V2403C series** **computer Using a Linux/Windows PC or Mac,** using PuTTY to open a remote terminal to Moxa computer on **Linux/Windows PC or Mac** and perform the following instructions in that window. 

Refer to the instruction at [Install the required tools and libraries for the AWS IoT Device SDK](https://docs.aws.amazon.com/iot/latest/developerguide/connecting-to-existing-device.html#gs-device-sdk-tools) and [Install AWS IoT Device SDK](https://docs.aws.amazon.com/iot/latest/developerguide/connecting-to-existing-device.html#gs-device-install-sdk) for Python on Moxa V2403C series computer directly. Follow the steps outlined in these sections to install AWS IoT Device SDK for your Moxa computer:

- Update the operating system and install required libraries
- Install git
- Install the AWS IoT Device SDK for Python.

Note: Due to using Python, there is no need to compile/build any programs. And we perform all steps in Moxa computer, there is no need to load/upload any programs to it.

# Run the demo

Continue previous section, perform the instructions, [Install and run the sample app](https://docs.aws.amazon.com/iot/latest/developerguide/connecting-to-existing-device.html#gs-device-node-app-run), in that terminal window. 

To view the MQTT messages published by the sample app in the AWS IoT console, perform the instructions,[View messages from the sample app in the AWS IoT console](https://docs.aws.amazon.com/iot/latest/developerguide/connecting-to-existing-device.html#gs-device-view-msg).

# Debugging

1. Not able to login Moxa V2403C series computer's through SSH terminal.

    Connect a display monitor to the Moxa V2403C series computer, and then power it up. Once the system is ready, a login screen will appear on your monitor. Refer to Starting from a VGA Console of [**Moxa V2403C series computer-linux-user-manual](https://cdn-cms.azureedge.net/getmedia/a116920c-a18a-428b-89b3-5ef9e3912309/moxa-v2403c-series-linux-manual-v1.0.pdf)** for the detail steps. After login Moxa computer check following items:

    a. Check if IP address of LAN1/LAN2 is in the same subnet of your PC.

    b. Check if you are able to operate OS normally. If not, gather all error message when you operate OS and then [CONTACT US](https://www.moxa.com/en/support/technical-support)

2. Moxa computer is not able to access internet.

    a. Check if IP address, mask and gateway of LAN1/LAN2 are configured in /etc/network/interfaces properly.

    b. Check if routing is correct.

    c. Check if nameserver is configured in /etc/resolv.conf

# Troubleshooting

Still need assistance with your Moxa product? [CONTACT US](https://www.moxa.com/en/support/technical-support)
