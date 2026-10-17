# Alpha-C Bell System

**Automated school bells, precision scheduling and emergency tones — running fully offline on your own network.**

Alpha-C Bell System drives the audio hardware already in your building: an onboard sound card, a USB or multi-channel interface, Dante (through DVS) or AES67 network audio. Every output becomes a bell zone with its own schedule. It runs on an air-gapped LAN, sends nothing to the internet, and is built to keep ringing unattended for years.

This repository is where the **Windows installer** is published. The source code is not public — see [Licence](#licence).

Website and full release history: **[alphabellsystems.com](https://alphabellsystems.com)**

---

## Download

**[⬇ Download the latest release](https://github.com/warlockscript/Alpha-Bell-System-public/releases/latest)**

Open the latest release and download the file named `AlphaCBellSystem_Setup_Education_<version>-SE.exe` under **Assets**.

- **Free 30-day evaluation.** Every feature works during the evaluation; a licence file keeps it running afterwards.
- **Same installer for evaluation and licensed use.** Buying a licence does not mean reinstalling — you load the licence file you receive.

### Check your download

Each release lists the installer's SHA-256 checksum. To confirm the file arrived intact, run this in PowerShell in the folder you downloaded to, and compare the result with the release page:

```powershell
Get-FileHash .\AlphaCBellSystem_Setup_Education_*.exe -Algorithm SHA256
```

The installer is not yet code-signed, so Windows SmartScreen may show *"Windows protected your PC"*. Choose **More info → Run anyway** only if the checksum matches.

---

## System requirements

| | |
|---|---|
| **Operating system** | Windows 10 version 1903 or newer, or Windows 11 — 64-bit |
| **Install rights** | Administrator (installs a watchdog service) |
| **Audio** | Any output Windows can see: onboard, USB, multi-channel PCIe, Dante Virtual Soundcard, AES67 |
| **Network** | None required. Federation and the web admin use your own LAN only |
| **Internet** | Never required — not for installing, licensing or running |

### Before you rely on it after a power cut

A bell system has to come back on its own. That depends on Windows **signing in automatically** after a restart — otherwise the PC stops at the login screen and no bell rings until someone signs in. The installer checks this and warns you; *Help → System Health → Power-Loss Recovery* reports it at any time. Ask your IT staff to configure Windows automatic logon for the account that runs the bell system.

---

## Install

1. Download the installer (above) and check its SHA-256.
2. Run it as an administrator and accept the licence agreement.
3. Start **Alpha-C Bell System** from the Start menu; the setup wizard walks you through your zones and audio outputs.
4. To license it, use **Help → Activate License…** and load the licence file you were sent.

The User Manual (PDF) is installed with the program — press **F1** or use *Help → User Manual*.

---

## Buying a licence

Licences are per installation and set the edition and zone count (8 to 48 zones). See **[pricing](https://alphabellsystems.com/pricing)** or **[contact us](https://alphabellsystems.com/contact)** for a quotation or an invoice for your school's purchasing office. Updates within your licence line are free.

---

## What's in each release

Every release has notes on the [Releases page](https://github.com/warlockscript/Alpha-Bell-System-public/releases), written for the people who run the bells rather than for developers. The complete history is at [alphabellsystems.com/whats-new](https://alphabellsystems.com/whats-new) and inside the program under *Help → What's New*.

### Coming soon

**Bell nodes** — a small box per building that adds eight zones on your own network. In development; not part of the current release.

---

## Important: not a certified fire alarm

Alpha-C Bell System is a scheduling, paging and **supplementary** notification aid. It is not a certified fire-alarm, life-safety or emergency-communication system (UL 864, UL 2572, EN 54, NFPA 72 or similar), and it must not be the sole or primary means of alerting people to an emergency. Keep your code-required certified systems in place and tested. See section 1 of the [licence agreement](LICENSE).

---

## Licence

Alpha-C Bell System is **proprietary software**, licensed — not sold — under the end-user licence agreement in [`LICENSE`](LICENSE). That is the same agreement the installer shows. Downloading the installer for evaluation is free; continued use requires a licence file.

The program includes third-party components (Qt, FFmpeg, OpenSSL, Piper text-to-speech and others) under their own licences. Their notices are in [`THIRD-PARTY-NOTICES.txt`](THIRD-PARTY-NOTICES.txt) and the full licence texts in [`licenses/`](licenses/). Qt and FFmpeg are dynamically linked and can be replaced as their LGPL licences allow.

## Support

Email **masterpro0115@gmail.com** — please include your version (*Help → About*) and, for a problem, the day's log file from `C:\ProgramData\Alpha-C Bell System\logs`.

© Master Pro Sounds & Lights Services, Philippines. All rights reserved.
