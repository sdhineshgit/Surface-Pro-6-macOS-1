 Surface Pro 6 Black (Hackintosh)  Apple CLOVER profile  (Translated From Chinese)

After the MacBook Pro, the Surface Pro6 is a machine I really like. The host is 770g + keyboard 310g + pen 20g = 1100g! Very lightweight. Based on my love of Surface Pro6, I have made 4 tutorials to help more Surface Pro6 users worry free.

    Surface Pro6 super detailed tutorial has a total of 4 series:

    Surface Pro 6 ultra-detailed tutorial with dual installation of windows10 and black apple macOS 10.14;

    Reprinting of the above series of tutorials is not authorized. 

Configuration information

    Brand model: Microsoft Surface Pro 6 fanless version
    CPU: Core i5-8250U
    Graphics: UHD Graphics 620 128MB
    Memory: 8GB
    Sound Card: ALC298
    Display: LGD0555 12.3 inches
    Display ratio: 3: 2
    Resolution: 2736 x 1824
    Hard Drive: SK HYNIX Skhynix BC501 NVMe 128GB 

About the solution of the card in Tianzi:

Two ultimate solutions for restarting stuck in the Tian word logo interface:

1. Under Win, use DG to enter the ESP partition, delete all three directories at the beginning, and then shut down and wait for 20-60 seconds and then boot up to enter clover boot. If you still can't enter the clover interface, continue to force shut down and wait for 1 minute before turning it on again.

2. If your EFI is installed on a mobile device, remove the mobile storage device after forced shutdown and then plug it in to identify it.

In addition, after installing the black apple, all EFI file updates must be performed under macOS, and this situation will not be encountered, no matter which EFI is installed on the device.

Solutions for WiFi:

Use COMFAST USB wireless network card, model: COMFAST CF-915AC, COMFAST CF-811AC, COMFAST CF-WU810N

Using this driver is very stable: link: https://pan.baidu.com/s/1aaUNqg6BJxlPxeq4WoTgSw password: y9b0
About Bluetooth solution:

Using Green Alliance's USB Bluetooth (white without lanyard hole CSR8510 A10 chip), the macOS system is directly driver-free and can be identified by plugging in. It can connect multiple keyboards, mice, headphones, AirPods2 (perfect) simultaneously.
About wireless network card Bluetooth 2-in-1 USB device:

Yuezhirenxin 5G wireless network card Bluetooth 2-in-1 USB device tested by Pro6 user chase69 feedback that Bluetooth cannot be used
About using USB Bluetooth / Wireless Mouse Keyboard Stalling Solution:

Use a powered USB3.0 hub and a USB2.0 hub to perform well in daily use. USB3.0 HUB (0.6m) plugged into a 1TB SSD U disk; USB2.0 HUB (0.2m) plug: USB wireless network card, USB Bluetooth receiver, wireless mouse / mechanical keyboard.

If you use the to go system like me and will use it on Surface Pro6, USB3.0 hub is best to buy RTS5411 chip with power supply, which can prevent sudden restart.
How to enable the touchpad:

Put the two files VoodooI2C.kext and VoodooI2CHID.kext in EFI / CLOVER / OEM / Surface Pro 6 / UEFI / kexts / into the / System / Library / Extensions / directory and then rebuild the cache to use the touchpad perfectly.

/ System / Library / Extensions / The Chinese path in your system is: macOS / System / Resource Library / Extensions /
External display blur solution:

Please go to: Surface Pro6 Black Apple External Display Turn on the native HiDPi display effect Follow the tutorial to turn on HIDPI with one click, which perfectly solves the problem of blurred external display.
Black Apple Mirror for Surface Pro6

Surface Pro6 installation image: Surface Pro6 black apple image macOS Mojave 10.14.6 official version with Clover 4968

For the 10.14.4 installation with config-Instll to enter the infinite restart of the system, please move the cursor to the macOS icon on the CLOVER interface and press the space to enter the boot setting interface, select "Block injected kexts" to enter the interface for prohibiting the driver, and select the 10.14 driver directory , Then check "SMCBatteryManager.kext" to disable the battery driver, press ESC to return to the main interface and select config-Intall into the system to rebuild the cache.
Update information:

Please use Clover Configurator on macOS to open the EFI partition where the black apple configuration is located, then delete the BOOT and CLOVER directories under the EFI / directory, and then drag the BOOT and CLOVER directories in the downloaded EFI file to the system EFI / directory to complete the update. .

2019/05/10: As the CHIPFANCIER NANO 1TB SSD was scrapped some time ago, all photos, design materials and other data stored in these years are gone. During this period of time, I didn't have to worry about it. In the past two days, I have just equipped new equipment to make a usable system and specially updated a wavelet. Because the original CLOVER theme is too large (28MB), it will affect the startup speed. A new 4K theme is specially designed. The entire file size is about 4MB. The default background can be changed freely.

    Wait for time to send 10.15 configuration
    2019-09-08:
        v2.3
        Update CLOVER 4968
        Updated macOS 10.14-10.14.6 full series support
        Updated macOS 10.14-10.14.6 full series SD card support
        Update AppleALC
        Update Lilu
        Update WhateverGreen 
    2019-05-26:
        v2.2
        Update CLOVER 4934
        Supports macOS 10.14.5 
    2019-05-10:
        v2.1
        Update CLOVER 4928
        Update VirualSMC 1.0.3
        Add new default theme XBlue 
    2019-04-24:
        v2.0
        Update CLOVER 4922
        Fixed the problem of small horizontal screen when driving the graphics card in the second stage of booting
        Add a Config-D-Display.plist file for external display. You can close the internal screen by adjusting the brightness or closing the keyboard cover.
        By far the most stable EFI version 
    2019-04-22:
        v1.9.2
        Fix 10.14.2 infinite restart problem
        Use native frequency conversion
        Remove CPUFriend.kext
        Remove CPUFriendDataProvider.kext 
    2019-04-16:
        v1.9.1
        Update VoodooI2c 2.1.5
        Update AppleALC 1.3.7
        Update WhateverGreen 1.2.8
        Added SMCBatteryManager.kext
        Remove ACPIBatteryManager.kext 
    2019-04-08:
        v1.9
        Update CLOVER 4919
        Fix Apple icon size display when entering system first stage
        Remove version prompt before loading CLOVER
        Remove the default profile EDID injection information 
    2019-04-02:
        v1.8
        Update CLOVER 4915
        Update drivers64UEFI driver
            Add AudioDxe-64.efi 
    2019-03-31:
        v1.7
        Update CLOVER 4912
        Update liu 1.3.5
        Update AppleALC 1.3.6
        Update USBInjectAll 0.7.1
        Cancel the lowest 800MHz frequency conversion
        Regenerate new frequency conversion file 
    2019-03-29:
        v1.6
        Update CLOVER 4910
        Fix brightness save
        Streamline and update drivers64UEFI
            Remove AudioDxe-64.efi
            Remove Fat-64.efi
            Remove UsbKbDxe-64.efi
            Remove UsbMouseDxe-64.efi
            Remove VBoxHfs-64.efi
            Update EmuVariableUefi-64.efi
            Update HFSPlus.efi 
        Remove CodecCommander.kext
        Remove VoodooPS2Controller.kext
        Added VoodooI2C.kext
        Added VoodooI2CHID.kext
        VoodooI2C.kext and VoodooI2CHID.kext, put them in the / System / Library / Extensions / directory and rebuild the cache to use the touchpad 
    2019-03-26:
        v1.5
        Update CLOVER 4903
        Support 10.14.4 official version
        You must select the config-Install configuration file when restarting multiple times during the installation of the 10.14.4 update. After the update is completed, you must rebuild the cache. After the cache is rebuilt, you can restart the system using the default configuration file 
    2019-03-22:
        v1.4
        Update CLOVER 4901
        The default boot system is macOS, please make sure you follow the tutorial to format the macOS partition name as macOS, otherwise you need to modify it yourself 
    2019-03-15:
        v1.3
        Update CLOVER 4896 
    2019-02-24:
        v1.2
        Counterfeit a useless en0 network card so that the USB wireless network card can pass Apple ID verification 
    2019-02-23:
        v1.1 
    2019-02-21:
        v1.0 

Currently completed:

    Internal screen display is normal;
    Brightness adjustment is normal;
    The external HDMI is normal, and the internal screen can be used at the same time;
    ALC298 is built-in normally;
    Built-in SD card slot is normal;
    Hibernation
    Built-in fake en0 network card;
    Siri is used normally;
    iCloud login is normal;
    App Store login is normal, download is normal;
    iMessage login is normal
    The power button is normal. Press the key for three seconds to display the key menu. Press the switch for one second.
    Trackpad is normal 

Items not carried out:

    Volume +-button;
    Power display;
    There is no global solution: touch screen, built-in Bluetooth, built-in WiFi, camera;
    Looking forward to your perfect sharing! 

System screenshot

