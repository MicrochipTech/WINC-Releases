# WINC1500 Release History

This document summarises the firmware and driver releases for the Microchip ATWINC1500 Wi-Fi module.

## Release Version 19.7.11 (Latest)

### ASF3 Packages
- [WINC1500 Firmware Update Project](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC1500/19_7_11/WINC1500_FIRMWARE_UPDATE_PROJECT.7z)
- [Wi-Fi Host Driver](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC1500/19_7_11/host_drv.zip)

### Release Details
- Fixed a TLS root certificate validation bypass vulnerability introduced in 19.7.10, where self-signed certificates were accepted without verification
- Fixed OTA issue that could result in erroneously switching to an invalid image
- Fixed DHCP client sending an empty host name (option 12), preventing IP address assignment from strict DHCP servers
- Multiple OTA robustness improvements including better error reporting and socket conflict prevention
- MAC address handling now uses a MAC address in efuse if it looks valid even if the "MAC Address Used" bit is not set
- Fixed WPA2 Enterprise connection attempts that could sometimes take up to 30 seconds due to dropped EAP Identity Request frames
- TLS Server mode with ECDHE-RSA ciphersuites no longer requires an ECDSA certificate chain
- All mandatory MISRA C coding standard warnings resolved in ASF driver code

---

## Release Version 19.7.10

### ASF3 Packages
- [WINC1500 Firmware Update Project](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC1500/19_7_10/WINC1500_FIRMWARE_UPDATE_PROJECT.7z)
- [Wi-Fi Host Driver](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC1500/19_7_10/host_drv.zip)

### Release Details
- Allow enabling/disabling of specific Phase 1 WPA Enterprise methods
- Added EAPOL v3 support for WPA Enterprise connections
- Fixed connection parameter saving code to ensure it doesn't make unnecessary flash writes
- Correctly parse and handle the "critical" field of x.509 certificate extensions
- Check CA Basic Constraint in TLS certificate chain

---

## Release Version 19.7.7

### ASF3 Packages
- [WINC1500 Firmware Update Project](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC1500/19_7_7/WINC1500_FIRMWARE_UPDATE_PROJECT.7z)
- [Wi-Fi Host Driver](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC1500/19_7_7/host_drv.7z)

### Harmony3 Packages
- [wireless_wifi Repository](https://github.com/Microchip-MPLAB-Harmony/wireless_wifi)
- [wireless_apps_winc1500 Repository](https://github.com/Microchip-MPLAB-Harmony/wireless_apps_winc1500)

### Release Details
- Fix to ignore unknown OUI in message 3 of 4-way handshake
- Fixed handling of source address when forwarding ARP packets out from the host
- Added SSL options such as SNI and server name verification in OTA

---

## Release Version 19.7.6

### ASF3 Packages
- [WINC1500 Firmware Update Project](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC1500/19_7_6/WINC1500_FIRMWARE_UPDATE_PROJECT.7z)
- [Wi-Fi Host Driver](https://github.com/MicrochipTech/WINC-Releases/raw/refs/heads/master/WINC1500/19_7_6/host_drv.7z)

### Release Details
- Countermeasures for 'Fragattack' vulnerabilities

---

## Additional Resources

- [ATWINC1500 Product Page](https://www.microchip.com/en-us/product/ATWINC1500)
- [Firmware Update Guide](https://support.microchip.com/s/article/How-to-update-the-firmware-of-WINC1500-module)
- [OTA Firmware Upgrade Guide](https://microchipsupport.force.com/s/article/How-to-upgrade-the-firmware-using-OTA-application-and-supported-firmware-releases)
