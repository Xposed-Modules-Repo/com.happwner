<p align="center">This is a shortened version of README. You can <a href="https://github.com/Omegaplexx/Happwner">view the full version in source repository</a></p>

# Happwner

Xposed module for decrypting links and exporting subscriptions from the proxy utility [Happ](https://play.google.com/store/apps/details?id=com.happproxy) to any VPN apps (NekoBox, v2rayNG, Hiddify, and similar clients).

## Why?

To give users control over their subscriptions again, improve service transparency, and protect themselves from dishonest providers.

## Features

**Happwner** extracts clean VPN configurations and passes them into any applications.

Features:
* **One-click decryption of `crypt5` links** powered by the decryptor from **amurkanov**. All link versions are supported (from `crypt`, `crypt2`, etc. up to `crypt5`). Decryption does **not require** Happ, Xposed, LSPatch, or an internet connection.
* **HWID spoofing** when requesting a Happ subscription. Allows you to bypass the device limit and restore access to your subscription when switching devices;
* **Happ subscription update service** inside any apps (NekoBox, Hiddify, v2rayNG, husi, Exclave, Karing, etc.).

Features requiring **Xposed or LSPatch**:
* Interception of decrypted `crypt` links. This is an alternative decryption method and provides no advantages over the main method;
* HWID spoofing <u>inside Happ</u> and other target apps;
* Opening the interface with a three-finger tap gesture inside Happ or other target apps.

## Installation

### Xposed

1. Install Happwner and Happ;
2. Enable Happwner in your Xposed manager and select the recommended applications;
3. Restart Happ.

The app supports **Android 5.0+**.

### Without Root (LSPatch)

1. Install Happwner, Happ, [LSPatch](https://github.com/JingMatrix/LSPatch/releases) and [Shizuku](https://play.google.com/store/apps/details?id=moe.shizuku.privileged.api) (or [Split APKs Installer](https://f-droid.org/packages/com.aefyr.sai.fdroid) instead of Shizuku);
2. In the LSPatch manager, select **Happ** and choose a patch mode:
    * **Local**: patch and install the modified Happ, then select Happwner as the scope;
    * **Integrated**: embed the Happwner module, patch Happ, and install it.

#### Installing the patched APK

* **If the Shizuku service is running**, you can do this directly from the LSPatch manager;
* **If Shizuku is unavailable**, open Split APKs Installer (SAI), navigate to the *Download* folder, select all files containing `lspatched` in their names, and start the installation. <u>You may need to uninstall the original Happ first</u>.

**The modified Happ will launch successfully on the second attempt!** \
**LSPatch only supports Android 9 and above!**

## Acknowledgements

Special thanks to [amurcanov](https://github.com/amurcanov) for the [Happ Decrypt RS](https://github.com/amurcanov/happ-decrypt-universal) project. Happwner uses it as the primary method for link decryption.

## Disclaimer

I assume no obligations toward you as a user, do not guarantee the software will function correctly, and am not responsible for any actions you take.

Use this tool responsibly and do not create problems for VPN providers, otherwise you may get banned, and I will have to adapt the project to their new ridiculous restrictions.
