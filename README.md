# SenseiAQ
SenseiAQ app for connecting with Piera Systems IPS and Canāree sensors.

## Package Downloads
**[Windows 10 Installer](https://github.com/PieraSystems/SenseiAQ/releases/download/v1.2.3/SenseiAQ-1.2.3-Setup-Win.exe)**

**[MacOS Installer (10.15+ required)](https://github.com/PieraSystems/SenseiAQ/releases/download/v1.2.3/SenseiAQ-1.2.3-macOS.zip)**

## Installation Notes
**Windows 10** - If Microsoft Defender blocks the app, select "More info" and then "Run anyway". In some environments, manual installation of the [Silicon Labs driver](#driver-installation-windows-10) is required. 

**MacOS** - Secondary-click the app icon, then choose "Open" from the shortcut menu (currently awaiting Mac App Store approval).

## User Guide
* [SenseiAQ User Guide (PDF)](https://github.com/PieraSystems/SenseiAQ/releases/download/v0.9.5user-guide/SenseiAQ.User-Guide.V1.0.pdf)
* [SenseiAQ User Guide (DOCX)](https://github.com/PieraSystems/SenseiAQ/releases/download/v0.9.5user-guide/SenseiAQ.User-Guide.V1.0.docx)

## Updates
* October 7, 2021 - Version 1.2.3 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v1.2.3)).
* July 26, 2021 - Version 1.1.0 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v1.1.0)).
* June 6, 2021 - Version 1.0.0 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v1.0.0)).
* May 11, 2021 - Version 0.9.5 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v0.9.5)).

## Usage

Attach the sensor via USB and start SenseiAQ. Wait at least 1 minute for SenseiAQ to collect enough readings to calculate AQI.

Data can be viewed within SenseiAQ, saved to a log file, or sent to Azure's IoT Hub. Logs are stored in the SenseiAQ folder, inside the user's Documents folder.

## Troubleshooting

In some cases the device may be working but fails to communcate with SenseiAQ. If there's any other programs running that may be using communication ports, such as serial monitoring or logging software, it can prevent SenseiAQ from communicating with the device. Certain USB devices, such as IoT development boards, can also intefere with SenseiAQ's detection of the Piera/Canaree device.

Try shutting down any programs and unplugging USB devices that could potentially be interfering, then unplug the Piera/Canaree device and restart SenseiAQ. With SenseiAQ running, plug the device in again and wait up to a minute for it to start communicating.

## Driver Installation (Windows 10)

### IPS Series, Canāree A1, Canāree I1/I5

1. Download the [Universal Windows Driver](https://www.silabs.com/documents/public/software/CP210x_Universal_Windows_Driver.zip) from SiLabs.com.
1. Right-click on *CP210x_Universal_Windows_Driver.zip*, choose "Extract All..." and then "Extract".
1. Enter the *CP210x_Universal_Windows_Driver* folder and run *CP210xVCPInstaller_x64.exe*.
1. Follow instructions in Installation Wizard to complete installation.

### Canāree I1E

1. Download the [USB Windows Driver](https://www.olimex.com/Products/Breadboarding/BB-CH340T/resources/CH341SER.zip) from Olimex.com.
1. Right-click on *CH341SER.zip*, choose "Extract All..." and then "Extract".
1. Enter the *CH341SER* folder and run *CH341SER.EXE*.
1. Click Install button.
