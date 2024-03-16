# USBView-docs

How to use and Install **Universal Serial Bus Viewer in Windows**. 

[Japanese version](README.md)

USBView is a well-known tool for developers as a means of identifying problems related to USB hardware in Windows. It is a tool that anyone can use easily, but the installation procedure is a little complicated, so I will introduce it here.

## Installation overview

Please refer to the link below for details on what is written [here](https://learn.microsoft.com/windows-hardware/drivers/debugger/usbview).

[Universal Serial Bus Viewer in Windows](https://learn.microsoft.com/windows-hardware/drivers/debugger/usbview)

https://learn.microsoft.com/windows-hardware/drivers/debugger/usbview

1. Download and install the Windows SDK.

2. During the installation, select only the Debugging Tools for Windows box and clear all other boxes.

4. By default, on a x64 PC the SDK will install USBView to the following directory.

    **C:\Program Files (x86)\Windows Kits\10\Debuggers\x64**

 4. Open the kits debugger directory for the processor type you're running, and then select usbview.exe to start the utility.

## Windows SDK download

Please download the Windows SDK installer winsdksetup.exe from the SDK page below and launch it to begin the installation.

https://developer.microsoft.com/windows/downloads/windows-sdk/ 

![Launching the Windows SDK installer](sdk-e0.png)

### Launching the Windows SDK installer

When you start the downloaded winsdksetup.exe, the following screen will be displayed, so just click "Next" to start the installation. Select "Download the Windows Software Development kit - ..." to download the offline installer to another PC, etc.

![Launching the Windows SDK installer](sdk-e1.png)

### SDK installation item selection menu

The following is the panel for selecting features to install. By default, all features are enabled.

![SDK installation item selection menu](sdk-e2.png)

### Select to leave only **Debugging Tools for Windows**

To configure the installation, Leave only "Debugging Tools for Windows", the second one from the top, deselect the others and click "Install". You can select and leave other items, but they may not be available unless Visual Studio is installed.

![Select to leave only Debugging Tools for Windows](sdk-e3.png)

### Installation completed

After a while, the installation will be completed and a "Welcome" message will be displayed. Close it with the "Close" button.

![Installation completed](sdk-e4.png)

### Check the installation directory

When installing from this SDK, USBView for x64 PCs is installed by default in the following directory:

**C:\Program Files (x86)\Windows Kits\10\Debuggers\x64\usbview.exe**

Open the kits debugger directory for the processor type you are running and select usbview.exe to launch the utility.

![Windows SDK インストール](sdk-e5.png)

### Start USBView

This is an example of what is displayed when usbview.exe is started.
Each USB device is arranged in a tree structure via the USB Hub like this.
To obtain information about the target device, check the correspondence with the connection point and physical socket by plugging and unplugging the USB memory that serves as a landmark.

If you click on a normal USB device to display it, you can check the device information, device descriptor and endpoint information, etc.

![Start USBView](sdk-e7.png)

### Target device with problem

If a problematic USB target device is connected, it will be highlighted with a yellow "!" mark, as shown below.

![Target device with problem](sdk-e6.png)

### USBView source code

USBView source code is available in the Windows Driver Samples repository on GitHub.

https://github.com/microsoft/Windows-driver-samples/tree/main/usb/usbview

End of document.