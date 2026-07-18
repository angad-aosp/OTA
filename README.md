# LineageOS Downloads

### Requirements
The latest Android 16 firmware, an [unlocked bootloader](https://xdaforums.com/t/how-to-unlock-bootloader-on-xiaomi-hyperos-all-devices-except-cn.4654009/) and USB debugging enabled from developer options.

The latest LineageOS .zip package and boot, super_empty and vendor_boot .img files for xaga available [here](https://github.com/angad-aosp/OTA/releases).

The latest version of [Google's platform-tools](https://developer.android.com/tools/releases/platform-tools?hl=en#downloads) and a computer.

### First flash steps
Reboot to bootloader
```
adb reboot bootloader
```

Flash LineageOS recovery
```
fastboot flash boot boot.img
fastboot flash vendor_boot vendor_boot.img
fastboot wipe-super super_empty.img
```

Reboot to recovery
```
fastboot reboot recovery
```

Do a factory reset (Factory Reset > Format data / factory reset)

Sideload the LineageOS .zip package (Apply Update -> Apply from ADB)
```
adb sideload lineage-packagename.zip
```

Reboot to System

### Manually updating from recovery
Reboot to recovery
```
adb reboot recovery
```

Sideload the LineageOS .zip package (Apply Update -> Apply from ADB)
```
adb sideload lineage-packagename.zip
```

Reboot to System

### Manually updating from LineageOS Updater
Look at the [FAQS](https://github.com/angad-aosp/OTA/releases#faqs), question 4

### Reporting bugs / requesting features
Create an issue [here](https://github.com/angad-aosp/OTA/releases/issues) with the LineageOS exact version and steps on how to reproduce if it's an issue or what you want to be added into LineageOS.

Google Apps, Magisk, KSU and SafetyNet/Play Integrity related bugs/requests will be ignored and immediately closed !

Additionnally, if you aren't using exactly the same files available on the release section (ex: Using a different recovery like TWRP, a different kernel or being rooted), your issue will be ignored and immediately closed !

### FAQS
**Q1: How do I update my firmware after flashing LineageOS ?**

Answer: The latest firmware available for xaga is included on the LineageOS .zip package, hence keeping your firmware updated on each updates.

**Q2: Are Google Apps included with LineageOS ?**

Answer: No. This is a vanilla build; install Google Apps separately by following the [LineageOS GApps guide](https://wiki.lineageos.org/gapps/), Use arm64 package.

**Q3: Is the LineageOS .zip package is signed and passes SafetyNet and Play Integrity ?**

Answer: Yes its signed and passes basic integrity on play store

**Q4: How do I update to another release of LineageOS ?**

**OTA update**

Go to Settings -> System -> System Update, check for updates, then download and install the available update.

**Local update**

Download the latest LineageOS .zip package from the release page to your phone. Go to Settings -> System -> System Update -> Click on the three dots -> Local update, then select the downloaded .zip package. The updater will install it automatically.

**Q5: I've followed the steps for updating LineageOS localy but the update disapeared from the list before I clicked on the reboot option from the Updater**

Answer: It's a known bug with LineageOS updater with local updates, simply follow again the steps to add the LineageOS .zip packages from your smartphone storage into the updater and the update will be available again from the Updater app.

**Q6: How long can I expect a new release of LineageOS ?**

Answer: Most likely the following month or a few weeks later if it's not an **HOTFIX** release, you won't have an exact date/time however since I do this out of my free time.

**Q7: I love your work ! Can I give you a donation ?**

Answer: Of course ! You can simply do your donation at my PayPal [here](https://paypal.me/eliasgheeraert).

### Copyrights
Your warranty is now voided and I am not responsible for any bricks or bootloop.

Any apropriation/stealing and/or unauthorized redistribition of my work on the Internet without my constent is stricly forbidden.
