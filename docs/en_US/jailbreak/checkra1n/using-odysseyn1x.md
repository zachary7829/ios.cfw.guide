---
lang: en_US
title: Using Odysseyn1x
excerpt: Guide to installing checkra1n via Odysseyn1x
permalink: /using-odysseyn1x
pkgman: sileo
redirect_from:
  - /installing-odysseyn1x
  - /using-odysseynix
  - /odysseyn1x
  - /odysseynix
  - /using-bootra1n
  - /using-bootrain
  - /bootra1n
  - /bootrain
  - /using-checkn1x
  - /using-checknix
  - /checkn1x
  - /checkn1x
extra_contributors:
  - stekc
  - flowerible
  - bbaovanc
  - Tanbeer191
  - TheHacker894
  - zachary7829
---

::: warning

If you are using a computer with an AMD Ryzen CPU, you will likely run into issues. If you do run into issues, you should use a Mac or a computer with an Intel CPU to follow this guide.

:::

!!!include(./docs/en_US/jailbreak/checkra1n/include/semi-tethered.md)!!!

Odysseyn1x is a live bootable Linux environment that allows you to quickly run checkra1n on a compatible device. checkra1n is capable of jailbreaking millions of iOS devices with A7 to A11 SoC's on firmwares 12.0 to 14.8.1.

!!!include(./docs/en_US/jailbreak/checkra1n/include/odysseyra1n-explanation.md)!!!

On iOS 14: 
- Odysseyra1n is only fully supported on A8, A9, A10(X), and A11 devices. A8X and A9X devices are only fully supported up to 14.4.2 using an older version of checkra1n, with a special method required for A8X and A9X devices on 14.5 to 14.8.1, which is detailed at [Using Odysseyn1x (A9X)](/using-odysseyn1x-a9x).
-  A11 devices do not allow you to use SEP functionality in a jailbroken state. SEP functionality are things such as a passcode, Face ID/Touch ID, and Apple Pay.

## Requirements

- A 256MB or greater USB Drive
    - If you don't have a USB Drive, but do have another form of supported removable bootable hardware (e.g. A CD or DVD), you can use that instead of a USB Drive
- The latest version of [Odysseyn1x](https://github.com/raspberryenvoie/odysseyn1x/releases)
    - If you are on an A8X or A9X device, you should instead get the v2.9 release of [Odysseyn1x](https://github.com/raspberryenvoie/odysseyn1x/releases/tag/v2.9)
    - For 64-bit computers, download the "AMD64" version
    - For 32-bit computers, download the "i686" version
- [Ventoy](https://github.com/ventoy/Ventoy/releases)

![A screenshot of the Odysseyn1x menu](/assets/images/Odysseyn1x.png)

## Installing Ventoy

1. Download and extract the contents of the `Ventoy.zip` file
1. Insert your USB drive if you have not already done so, and open the `Ventoy2Disk.exe` file
1. Select the USB drive you would like to boot Odysseyn1x from
    - This USB drive will be completely erased
    - Ensure you back up all important data beforehand
1. Click `Install` and confirm that you are ok erasing the USB drive
    - Do not remove your USB Drive until the process has completed
1. Once it has installed, copy the Odysseyn1x iso file that you downloaded onto the USB drive

## Booting Odysseyn1x

1. Reboot, and then go into your BIOS settings and disable Secure Boot, then enter the boot picker and select your USB Drive to boot from
    - This is different for every computer
    - Search your PC or motherboard brand to find out how to get to your BIOS settings if you are unsure
1. Press enter once you see the Ventoy screen to boot into Odysseyn1x

## Running checkra1n

::: warning

If you are using a USB-C to Lightning cable to do this process, you may run into issues entering into DFU mode

If you do have issues, get a USB-A to Lightning cable and, if necessary, also get a USB-C to USB-A adapter.

:::

1. Once you have loaded odysseyn1x, select `checkra1n`
    - If you're on an A11 device, you will need to head into `Options`, then enable the `Skip A11 BPR Check` option once it runs
    - If you're on iOS 14.6 or later, you will need to head into `Options`, then enable the `Allow Untested Versions` option once it runs
    - If you're on an A8X or A9X device and are on iOS 14.4 to 14.4.2, you will need to head into `Options`, then enable the `Allow Untested Versions` option once it runs
1. Click `Start` and follow all onscreen prompts
1. You will now be presented with instructions in how to reboot your device into <router-link to="/faq/#what-is-dfu-mode">DFU mode</router-link>, click `Start` to begin
    - Follow the instructions until your device reboots to a black screen
1. Once your device boots, you can quit checkra1n, but do not shut down your computer

## The Odysseyra1n script

::: tip

If you would prefer to do so, instead of running the script on your computer, you can run the Odysseyra1n script using the [shortcut](https://www.icloud.com/shortcuts/8d4e206d568d4aadb624b2a6191a3771) by opening this page on your device and then clicking the shortcut hyperlink.

:::

The following steps only need to be performed once and are optional but highly recommended for a smoother experience and modern bootstrap.

1. Unlock your device
1. Ensure that your computer is trusted by your device
1. Select `Odysseyra1n` in Odysseyn1x
1. Sileo should install to your device
1. Do not close Odysseyn1x as you will need to re-jailbreak in a few minutes

!!!include(./docs/en_US/jailbreak/checkra1n/include/no-loader.md)!!!
!!!include(./docs/en_US/jailbreak/checkra1n/include/end-of-page.md)!!!
