[CyanogenMod](https://github.com/cyanogenmod/android/tree/cm-12.0)
=============

[Getting Started - Setup build environment](https://github.com/Arc-Team/android_vendor_arc/blob/pac-4.4/PrepareForBuild.md)
-------------------------------------------

To initialize on Linux:

    repo init -u git://github.com/Arc-Team/android.git -b cm-12.0 -g all,-notdefault,-darwin

To initialize on MacOS:

    repo init -u git://github.com/Arc-Team/android.git -b cm-12.0 -g all,-notdefault,-linux

Use our local manifests:

    Copy the file roomservice.xml located in "android/roomservice.xml"
    to ".repo/local_manifests/roomservice.xml"
    if the directory "local_manifests" not exist, create it!

Then to sync up:

    repo sync -f && repo sync -f

Then to build:

    . build/envsetup.sh && time brunch <device_code_name>

Example for HTC One XL:

    . build/envsetup.sh && time brunch evita
