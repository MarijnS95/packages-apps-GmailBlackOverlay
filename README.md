# Full-black RRO for Gmail

This turns the "Dark" mode in the android Gmail app into a full-black mode. Taking advantage of OLED panels and looking gorgeous overall.

Unfortunately the status- and navbar are still colored transparent grey. It is assumed these are hardcoded, or take+modify a different color. A similar thing happens to the search bar and the popup when clicking - the provided color has an extra tint added to it.

## HOWTO:
Either manually enable the overlay through `adb shell cmd overlay enable com.marijn.theme.color.gmail_black`, or turn this into a static overlay by adding `android:isStatic="true"` to the `overlay` element in [`AndroidManifest.xml`](./AndroidManifest.xml).

Note that a non-static overlay allows pushing the APK to the device and calling `cmd overlay enable` to reload it. There does not seem to be a way to update and reload static overlays without rebooting the phone.
