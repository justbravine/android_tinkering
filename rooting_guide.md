## Why would i want Root?
Root is basically obtaining Super User Permission to do pretty much anything at all in your Android device. From system-level debloating to major UI modifications and so on. Rooting has perks, lots of them, but it also has it's downsides such as voiding your warranty, loss of safetynet and playintegrity and blocked access to banking applications. These problems do have workarounds.
## Where do i start?
You will need a Compter
You must have downloaded and extracted your Device firmware zip file.
You must have unlocked your bootloader.
DO NOT SKIP STEP 2 AND 3!
## Steps to Follow
First off, download the latest stable magisk from the Repository
Now you will need the boot.img of your device which can be gotten inside your device firmware zip file.
Also in your firmware is the vbmeta.img file which is REQUIRED to DISABLE VERITY and BOOT VERIFICATION!
Put the boot.img file into your device and launch the Magisk application. Note: The boot image must be patched in the device that it will be flashed into. e.g Patch Tecno Spark 7 boot.img with Tecno Spark 7 and flash it to Tecno SPark 7.
Tap the "Install" button and select file for patching.
Search for your .img file and click it.
Once the patching process is complete, copy the file located in your Downloads Folder to your Computer along with the vbmeta.img located also in your firmware. This will be used to disable AVB (Android Verified Boot).
On your computer, put both image files in a folder and open your terminal in that folder.
Connect your device and run in terminal adb reboot bootloader
You must run the AVB disabling command before and after the boot image flashing command to avoid bootlooping
run fastboot --disable-verity --disable-verification flash vbmeta vbmeta.img to disable AVB
Now run fastboot flash boot patchedboot.img
Run the AVB command again and then, fastboot reboot
With all that done, you should be booted with Magisk properly installed.
