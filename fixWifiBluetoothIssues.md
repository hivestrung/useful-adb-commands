# Rooted Samsung Devices having Wifi and Bluetooth Issues

This issue pertains to rooted Samsung devices which lose Wifi and/or Bluetooth connection settings/password after returning to rooted **after booting in standard non-rooted mode**.

From Magisk Download download and install `libsecure_storage` and after rebooting your phone just go into Magisk Downloads, select libsecure_storage and read the description of the module (screenshots attached), the 5th paragraph is particularly relevant, yes, you definitely need to edit a file.

Use Root Broowser to locate the file `secure_storage_daemon.rc` and open it as a Text file selecting a text editor, and edit the last line to: `stop secure_storage` instead of `start secure_storage` then save it.

Job done, no more lost wifi or bluetooth credentials after booting non-rooted.

[Credits](https://forum.xda-developers.com/galaxy-s10/help/reboot-magisk-wifi-connect-problems-t3936158)
