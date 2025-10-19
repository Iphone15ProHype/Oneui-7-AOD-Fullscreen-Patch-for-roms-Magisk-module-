# Oneui 7 WALLPAPER ON AOD Patch for croms (Magisk module)
A universal Magisk module for One UI 7 devices that enables AOD fullscreen wallpapers by patching /system/etc/floating_feature.xml systemlessly. Only the AOD line is changed, preserving all other device-specific settings.
Disclaimer i am NOT repsonsible for any bricked devices this is just a small project made by me for my own use and i decided to make it public and open source for anyone to use!!!!

Installation/requirments:

Requirements:
Device: Any Samsung device running One UI 7 / Android 12+
The module is built for the One UI 7 XML structure.
Other Android versions or older One UI may not work.
Root: The device must be rooted via Magisk
Only Magisk supports systemless overlays required by the module.
Magisk Version: Magisk v29+ recommended
Tested on Magisk 29.0 (or newer).
Older versions may not run post-fs-data.sh or service.sh correctly.
Writable Module Path: The module requires /data/adb/modules/ to be writable
Standard on Magisk installations.
Existing XML: /system/etc/floating_feature.xml must exist
The module copies this file and only modifies the AOD line.
Devices with missing or heavily modified XML may not work.
SELinux: Must be enforcing or permissive
The module uses a bind mount to overlay the patched XML.
No Conflicting Modules:
Other Magisk modules that modify floating_feature.xml can cause conflicts.

Installation Steps:

1.Grab FloatingFeaturePatch_AOD_Universal_v1.0.zip from the repository or release page.
2.Open Magisk
3.Go to Modules → Install from storage.
4.Select the ZIP
5.Choose the downloaded module zip.
6.Flash the Module
7.Magisk will install it systemlessly.
8.Reboot Your Device (A full reboot is required for the patched XML to take effect.)
9.Verify if it works by:
Check that AOD fullscreen wallpapers now display properly.
You can also inspect /data/adb/modules/floating_feature_aod_patch/system/etc/floating_feature.xml to confirm the <SEC_FLOATING_FEATURE_LCD_CONFIG_AOD_FULLSCREEN> value is 1.
(incase of it not working join my discord server (link in profile))
