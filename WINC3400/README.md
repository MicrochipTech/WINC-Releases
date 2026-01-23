# WINC3400 Release History

This document summarises the firmware and driver releases for the Microchip ATWINC3400 Wi-Fi/BLE module.

## Release Version 1.4.8 (Latest)

### ASF3 Packages
- [WINC3400 Firmware Update Project](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC3400/1_4_8/WINC3400_FIRMWARE_UPDATE_PROJECT.zip)
- [Wi-Fi Host Driver](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC3400/1_4_8/wifi_drv.zip)
- [BLE Library](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC3400/1_4_8/winc3400_ble_api.zip)
- [BLE Service](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC3400/1_4_8/ble.zip)

### Release Details
- Fixed OTA issue that could result in erroneously switching to an invalid image
- Fixed WPA Enterprise connection failures with certain access points due to EAPOL exchange synchronisation issues
- TLS limitation where only 7 TLS records could be received in a single buffer, now increased to 51, improving MQTT protocol reliability
- Fixed ARP response frames containing corrupted Target MAC address field
- Fixed RSNE verification incorrectly requiring optional fields, preventing association with some access points
- Fixed DHCP client sending an empty host name (option 12), preventing IP assignment from strict DHCP servers
- Multiple OTA robustness improvements including better error reporting and socket conflict prevention
- MAC address handling now ignores possibly incorrectly programmed "MAC Address Used" bit in efuse

---

## Release Version 1.4.7

### ASF3 Packages
- [WINC3400 Firmware Update Project](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC3400/1_4_7/WINC3400_FIRMWARE_UPDATE_PROJECT.zip)
- [Wi-Fi Host Driver](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC3400/1_4_7/wifi_drv.zip)
- [BLE Library](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC3400/1_4_7/winc3400_ble_api.zip)
- [BLE Service](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC3400/1_4_7/ble.zip)

### Release Details
- Resolved an issue where the BLE MAC address was incorrectly set for odd Wi-Fi MAC addresses

---

## Release Version 1.4.6

### ASF3 Packages
- [WINC3400 Firmware Update Project](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC3400/1_4_6/WINC3400_FIRMWARE_UPDATE_PROJECT.zip)
- [Wi-Fi Host Driver](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC3400/1_4_6/wifi_drv.zip)
- [BLE Library](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC3400/1_4_6/winc3400_ble_api.zip)
- [BLE Service](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC3400/1_4_6/ble.zip)

### Release Details
- Added EAPOL v3 support for WPA Enterprise connections
- Fixed connection parameter saving code to ensure it doesn't make unnecessary flash writes
- Correctly parse and handle the "critical" field of x.509 certificate extensions
- Check CA Basic Constraint in TLS certificate chain
- Improvements and bug fixes to the BLE API
- BLE MAC address generation code no longer requires Wi-Fi MAC to be even

---

## Release Version 1.4.4

### ASF3 Packages
- [WINC3400 Firmware Update Project](https://github.com/MicrochipTech/WINC-Releases/blob/master/WINC3400/1_4_4/WINC3400_FIRMWARE_UPDATE_PROJECT.7z)
- [Wi-Fi Host Driver](https://github.com/MicrochipTech/WINC-Releases/blob/master/WINC3400/1_4_4/wifi_drv.7z)
- [BLE Library](https://github.com/MicrochipTech/WINC-Releases/blob/master/WINC3400/1_4_4/winc3400_ble_api.7z)

### Release Details
- TLS Subject Alternative Name support
- SNI and servername for OTA support (and other SSL options for OTA)
- Fixed failure to notify the host of a BLE disconnect in some scenarios
- Removal of some python scripts in the package as functionality is now native in the image_tool

---

## Release Version 1.4.3

### ASF3 Packages
- [WINC3400 Firmware Update Project](https://github.com/MicrochipTech/WINC-Releases/raw/master/WINC3400/1_4_3/WINC3400_FIRMWARE_UPDATE_PROJECT.7z)
- [Wi-Fi Host Driver](https://github.com/MicrochipTech/WINC-Releases/raw/master/WINC3400/1_4_3/wifi_drv.7z)

### Release Details
- Countermeasures for 'Fragattack' vulnerabilities
