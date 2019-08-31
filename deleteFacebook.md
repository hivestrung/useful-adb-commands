# Delete Facebook

The Samsung Galaxy S10 (and perhaps some other models) have Facebook installed as a system app.

This means you can't just uninstall it from your phone. You can only disable it.

Until now. Ensure adb is installed, adb debugging on your Android is enabled, connect via USB to your computer, launch Terminal/whatever and use the following commands:

# Launch adb shell

```bash
adb shell
```

# Uninstall Facebook

```bash
pm uninstall --user 0 com.facebook.services
pm uninstall --user 0 com.facebook.katana
pm uninstall --user 0 com.facebook.system
pm uninstall --user 0 com.facebook.appmanager
```

This does not uninstall Facebook Messenger. The package for Facebook Messenger is com.facebook.orca.

# To see the installed Facebook packages 

```bash
pm list package | grep facebook
