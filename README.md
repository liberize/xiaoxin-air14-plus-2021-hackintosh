# Hackintosh for Lenovo XiaoXin Air14 Plus 2021

This EFI aims to work with `macOS Monterey` now. Stay tuned :)

## Detail

| Item       | Detail                          | Works?  | Notes                   |
|------------|---------------------------------|---------|-------------------------|
| CPU        | AMD Ryzen 7 5800U               | Yes     | SMCAMDProcessor.kext    |
| Memory     | 16G                             | Yes     | Works |
| GPU        | AMD Vega 8 (iGPU)               | Partial | NootedRed.kext, have to disable gpu rasterization for chrome |
| HDMI       | AMD Vega 8 (iGPU)               | Yes     | NootedRed.kext |
| Brightness | Builtin Display                 | Yes     | BrightnessKeys.kext, add ACPI patch _OSI to XOSI and SSDT-XOSI |
| Audio      | ALC257                          | Yes     | AppleALC.kext, set layout-id=11 in DeviceProperties |
| Microphone | Builtin Microphone Array        | Yes     | AMDMicrophone.kext, place in /Library/Extension/ |
| Ethernet   | USB Adapter                     | Yes     | RealtekRT8111.kext? |
| WiFi       | Intel AX200                     | Yes     | AirportItlwm.kext, use OS-specific version |
| Bluetooth  | Intel AX200                     | Yes     | IntelBlueToothFirmware.kext + IntelBTPatcher.kext + BlueToolFixup.kext |
| Camera     | Builtin WebCam (USB)            | Yes     | See USB |
| Keyboard   | Builtin Keyboard                | Yes     | VoodooPS2Controller.kext? |
| TrackPad   | Builitin I2C TrackPad           | Yes     | VoodooI2C.kext + VoodooI2CHID.kext, disable VoodooInput.kext in VoodooPS2Controller.kext, load kexts in correct order |
| USB        | 2 Type-A + 2 Type-C             | Partial | USBToolBox.kext + UTBMap.kext, sometimes some port not working |
| SD Card    | BayHubTech SD Card Reader (PCI) | Yes     | CtlnaSDXC.kext, spoof device id in DeviceProperties |
| Battery    | Builitin Battery                | Yes     | SMCBatteryManagement.kext? battery percent is ok |
| Sleep      | -                               | No      | |
