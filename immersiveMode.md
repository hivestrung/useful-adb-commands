# Immersive Mode

On the S10, there's no way to hide the navigation bar buttons.
You can switch to Samsung's gestures but not everyone wants to do that
These commands will help you enable immersive mode in certain apps but show them in others.

## Launch adb shell

```bash
adb shell
```

## Enable immersive mode for all apps

```bash
settings put global policy_control immersive.navigation=*
```

## Disable immersive mode for all apps

```bash
settings put global policy_control immersive.navigation=null
``

## Customise the applications to hide navigation bar

### List your application packages

```bash
ls /sdcard/Android/data
```

A list of packages will appear, you can copy paste it into the below command

### Execute the command (example)

```bash
settings put global policy_control immersive.navigation="com.facebook.orca, com.android.chrome, org.telegram.messenger, com.whatsapp, com.google.android.apps.maps, com.google.android.youtube, com.instagram.android"
```

