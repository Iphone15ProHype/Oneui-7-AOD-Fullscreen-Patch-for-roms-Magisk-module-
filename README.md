# OneUI 7 Wallpaper on AOD Patch for Croms (Magisk Module)

A universal Magisk module for **One UI 7** devices that enables **AOD fullscreen wallpapers** by patching `/system/etc/floating_feature.xml` systemlessly. Only the AOD line is modified, preserving all other device-specific settings.

**Disclaimer:**
I am **not responsible** for any bricked devices or other problems caused by the module. This is a small personal project I decided to make public and open source for anyone to use.

---

## Requirements

* **Device:** Samsung device running **One UI 7**

  * The module is built for the One UI 7 XML structure.
  * Other Android versions or older One UI versions **may/ may not work** (Depends on multiple factors).
* **Root:** Device must be rooted via **Magisk**

  * Only Magisk supports the systemless overlay required by this module.
* **Magisk Version:** v29+ recommended

  * Tested on Magisk 29.0 or newer.
  * Older versions may not execute `post-fs-data.sh` or `service.sh` correctly.
* **Writable Module Path:** `/data/adb/modules/` must be writable

  * Standard on Magisk installations.
* **Existing XML:** `/system/etc/floating_feature.xml` must exist

  * The module copies this file and only modifies the AOD line.
  * Devices with missing or heavily modified XML may not work.
* **SELinux:** Must be **enforcing** or **permissive**

  * The module uses a bind mount to overlay the patched XML.
* **No Conflicting Modules:** Other Magisk modules that modify `floating_feature.xml` can cause conflicts.

---

## Installation Steps

1. Download `FloatingFeaturePatch_AOD_Universal_v1.0.zip` from the repository or release page.
2. Open **Magisk**.
3. Go to **Modules → Install from storage**.
4. Select the downloaded ZIP file.
5. Flash the module. Magisk will install it **systemlessly**.
6. **Reboot your device** (a full reboot is required for the patched XML to take effect).
7. Verify it works:

   * AOD fullscreen wallpapers should now display correctly.
   * You can check `/data/adb/modules/floating_feature_aod_patch/system/etc/floating_feature.xml` to confirm that `<SEC_FLOATING_FEATURE_LCD_CONFIG_AOD_FULLSCREEN>` is set to `1`.

**Need help?**
If it’s not working, join my Discord server (link in profile).

**FunFact:** This module was originally made for my Samsung S20+ 5G on Extreme ROM Nexus v.2.6.1  
(I recommend using this exact ROM with the module)


---

