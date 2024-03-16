# USBView-docs

How to use and Install **Universal Serial Bus Viewer in Windows**. 

[Japanese version](README.md)

Please refer to the link below for details on what is written [here](https://learn.microsoft.com/windows-hardware/drivers/debugger/usbview).

[Universal Serial Bus Viewer in Windows](https://learn.microsoft.com/windows-hardware/drivers/debugger/usbview)

https://learn.microsoft.com/windows-hardware/drivers/debugger/usbview

## How to install USBView

1. Download and install the Windows SDK.

2. During the installation, select only the Debugging Tools for Windows box and clear all other boxes.

4. By default, on a x64 PC the SDK will install USBView to the following directory.

  **C:\Program Files (x86)\Windows Kits\10\Debuggers\x64**

  Open the kits debugger directory for the processor type you're running, and then select usbview.exe to start the utility.

To configure the installation, select only the Debugging Tools for Windows box and deselect all other boxes.

When installing from this SDK, USBView for x64 PCs is installed by default in the following directory:

C:\Program Files (x86)\Windows Kits\10\Debuggers\x64


Open the kits debugger directory for the processor type you are running and select usbview.exe to launch the utility.

USBView source code

USBView is also available in the Windows Driver Samples repository on GitHub.


実行中のプロセッサの種類の kits デバッガー ディレクトリを開き、[usbview.exe] を選択してユーティリティを起動します。

USBView ソース コード

USBView は、GitHub の Windows ドライバー サンプル リポジトリでも入手できます。

##

https://developer.microsoft.com/windows/downloads/windows-sdk/ のページでWindows SDK インストーラー winsdksetup.exe をダウンロードして起動し、インストールを開始します。

![Windows SDK インストール](sdk-e0.png)

winsdksetup.exe を起動すると次の画面が表示されるので、そのまま「Next」でインストールを開始します。下の選択は別のPC等へのオフラインインストーラをダウンロードする場合に選択します。

![Windows SDK インストール](sdk-e1.png)

インストール機能の選択画面です。デフォルトでは全ての機能が有効です。

![Windows SDK インストール](sdk-e2.png)

上から2番目の「Debugging Tools for Windows」だけを残して、他のチャックを外して「インストール」をクリックします。

![Windows SDK インストール](sdk-e3.png)

しばらく経つとインストールが完了して「Welcome」メッセージが表示されます。「Close」ボタンで閉じます。

![Windows SDK インストール](sdk-e4.png)

この手順でインストールした場合、x64版実行モジュールのインストール先は、
C:\Program Files (x86)\Windows Kits\10\Debuggers\x64\usbview.exe となります。

![Windows SDK インストール](sdk-e5.png)

そのまま usbview.exe を起動した場合の表示例です。
この様に 問題があるUSBデバイスが接続している場合は、黄色「!」マークで強調表示されます。

![Windows SDK インストール](sdk-e6.png)

正常なUSBデバイスをクリックして表示させると、デバイス情報、デバイスディスクリプターとエンドポイントの情報などを確認することが可能です。

![Windows SDK インストール](sdk-e7.png)

USBの各デバイスはこの様にUSB Hub を介してツリー構造で配置されます。
目的のデバイスの情報は目印となるUSBメモリーを抜き差しする等して接続点、物理ソケットとの対応を確認します。

以上。