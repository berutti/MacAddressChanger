# MacAddressChanger
Temporary MAC address changer. 

Allows you to set a temporary MAC Address on a network interface of your choice on Linux.
This will allow you, for example, to authorize headless/keyboardless devices of your own 
through a captive portal (e.g: Wii, Google Chromecast, Wi-Fi smartwatches, TV set top boxes, etc).

This is a simple .sh script, just launch it as root with the following parameters:

    macchange INTERFACE TEMP:MAC:ADDRESS:00:00

The interface name should match the name that you can find on ifconfig and the new mac address should be as reported on your device. Digits should be separated by ":"

Eg:
    root@your_machine:/path/to/script# ./macchange wlan0 00:00:00:00:00:00

The new mac-address should be of the peripheral you want to impersonate, or authorize through a captive portal. Please switch the peripheral whose MAC you are cloning before doing it or you will generate network conflict.

If you have to authorize the peripheral through a captive portal, once changed the mac-address please try to navigate with your browser and log-in. Then go back to the script and confirm with <ENTER> that you want to restore your initial address.
That's it.
