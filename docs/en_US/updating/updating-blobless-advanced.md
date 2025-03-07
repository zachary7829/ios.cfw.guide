---
lang: en_US
title: Updating (Blobless) (Advanced)
description: Guide on updating to unsigned firmwares without any blobs.
permalink: /updating-blobless-advanced
extra_contributors:
  - flowerible
---

## Required Reading

iOS and iPadOS devices can typically only update to firmware versions which Apple has "signed". This usually means that you can only update to the most recent firmware versions. This is bad for jailbreaking, as most jailbreaks rely on exploits that have been patched in newer versions.

Fortunately, we can use different "profiles" to delay a firmware update. This is intended for organisations which require additional time to update their devices, however we can also use these to update to unsigned firmware versions.

This has a time limit, however. You will only be able to update to the following firmware versions before their respective expiration dates:

- **15.3.1** - June 13th, 2022
- **15.4** - June 29th, 2022
- **15.4.1** - August 14th, 2022

Time is given in `UTC 00:00`. For more expiration dates, view [dhinakg.github.io/delayed-otas.html](https://dhinakg.github.io/delayed-otas.html).

Because you do not currently have a jailbreak (or you choose not to jailbreak for any reason), you'll have to use advanced methods, involving things such as resetting all contents and settings, to be able to update.

::: danger

Depending on your target iOS version, you won't be able to do this if you futurerestored after the following dates:

  - 15.3.1: March 14th, 2022
  - 15.4: March 31st, 2022
  - 15.4.1: May 16th, 2022

:::

## Preparing

1. Plug your iDevice into your computer and make a backup through iTunes or Finder

After making a backup, what you need to do after is dependent on if you use macOS or Windows

## macOS - Apple Configurator 2

1. Go to the App Store on your Mac
1. Search for `Apple Configurator 2` and install it
1. Setup Apple Configurator 2
1. Click Get Started
1. Click on your device, and then click Prepare
1. Select `Manual Configuration`
1. Choose `Do not enroll in MDM`
1. Go to `Organization`, and click `New Organization`
1. Either sign in to your Apple ID, or click Skip
    - If you chose to skip signing into your Apple ID, add a name, then click Next
1. Choose `Generate a new supervision identity`
    - If you've done this before in Apple Configurator 2, you can `Choose an existing supervision identity` instead
1. Configure the iOS Setup Assistant as you wish
    - If you forgot to backup your data earlier in the guide, this is the last step where you'll be able to do this.
1. Click `Prepare`, which will erase your device and supervise it

## Windows - iMazing

::: danger

This method requires that you purchase iMazing, if you don't have money to purchase iMazing, you cannot follow this method

:::

1. Download and install iMazing from [here](https://imazing.com/download/windows)
1. After setting up iMazing, click the `Supervision` option
1. Click Next, click the button below `Organization`, then click Choose
1. Click the `+` button at the bottom left corner of the new window
1. Add a name, then click `Save`
1. Click Choose, then click Next
    - If you forgot to backup your data earlier in the guide, this is the last step where you'll be able to do this.
1. Type the number it lists into the text box, then click `Next`, iMazing will erase your device and supervise it

## Updating your firmware version

1. When the device boots up after being erased, set it up, then open this page on your device
1. Tap a version below to install its respective update profile:
    - [15.3.1](/assets/files/delay_15_3_1.mobileconfig)
    - For more firmware versions, view [dhinakg.github.io/delayed-otas.html](https://dhinakg.github.io/delayed-otas.html).
1. Reboot your device
1. Plug your device into power and connect to the Internet with Wi-Fi
1. Open the Settings application
1. Tap `General` -> `Software Update`
1. Ensure that the version displayed is the version you are intending to update to
1. Download and install the update
1. Once updated, remove the update profile through Settings

After updating, you can remove supervision and restore your backup you made earlier by erasing all content and settings.

If you're having issues with updating, install [OTAEnabler](https://repo.cadoth.net/) and reboot. If you're still having issues continue reading below. 

::: tip

If the update was successful, continue to [Get Started](/get-started) to jailbreak your device.

:::

## Troubleshooting

### "iOS is up to date"

1. Remove any beta profiles installed
1. Install the OTADisabler tweak and then uninstall it
1. Restart your device
    - You can also use ldrestart or a userspace reboot

### "Unable to check for updates"

1. Restore rootFS through your jailbreak
1. Install and open the <router-link to="/installing-unc0ver">unc0ver</router-link> application
1. Turn off "Disable updates"
1. Re-jailbreak using unc0ver

### It just freezes

Re-enable the OTA daemon using the iCleaner tweak

---

Credits to [dhinakg](https://github.com/dhinakg/) for discovering this method.
