<p align="center">This is a shortened version of README. You can <a href="https://github.com/Omegaplexx/Happwner">view the full version in source repository</a></p>

# Happwner

Xposed module for decrypting and exporting subscriptions from the proxy utility [Happ](https://play.google.com/store/apps/details?id=com.happproxy) to any VPN apps (NekoBox, v2rayNG, Hiddify, and other).

## Why?

To give users control over their subscriptions again, improve service transparency, and protect themselves from dishonest providers.

## Features

**Happwner** extracts clean VPN configurations while bypassing artificial restrictions.

The application:
* Intercepts the **real** subscription links if they are encrypted (`happ://crypt5`).
* Spoofs and persists the HWID inside Happ to bypass device limits or restore access after changing devices.
* Can run a local service that allows third-party apps (NekoBox, v2rayNG, etc.) to update Happ subscriptions without leaving their interface;
* Supports opening the interface with a three-finger tap gesture inside Happ;
* Supports all Android versions compatible with Happ — **Android 5.0+ (Lollipop)**.

## Installation

1. Install Happwner;
2. Enable the module in your Xposed manager (EdXposed/LSPosed/Vector);
3. Select **Happ** (`com.happproxy` and/or `su.happ.proxyutility`) as the target app;
4. Restart Happ.

## Disclaimer

I assume no obligations toward you as a user, do not guarantee the software will function correctly, and am not responsible for any actions you take.

Use this tool responsibly and do not create problems for VPN providers, otherwise you may get banned, and I will have to adapt the project to their new ridiculous restrictions.
