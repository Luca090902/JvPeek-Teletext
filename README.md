# JvPeek-Teletext
Teletext-Port von JvPeek's Webseite / Teletext port of JvPeek's website

## Voraussetzungen / Requirements
* Raspberry Pi
* Raspberry Pi OS (32-Bit) | 64-Bit-Version wird nicht unterstützt. / 64 bit version isn't supported.
* Composite-Cinch-Adapter
* VBIT2

## Vorkonfiguration / Pre-Configuration
### Deutsch
* /boot/config.txt mit Root-Rechten bearbeiten
* Kommentar bei `#sdtv_mode=2` entfernen -> `sdtv_mode=2`
* `dtoverlay=vc4-kms=v3d,composite` und `max_framebuffers=2` auskommentieren oder entfernen
* Speichern
* `sudo raspi-config`
* Display Options -> Composite -> V2 Enable Composite
* Neustarten

### English
* Edit /boot/config.txt with root permissions
* Remove comment at `#sdtv_mode=2` -> `sdtv_mode=2`
* Command out or remove `dtoverlay=vc4-kms=v3d,composite` and `max_framebuffers=2`
* Save
* `sudo raspi-config`
* Display Options -> Composite -> V2 Enable Composite
* Reboot

## Installation
* `cd ~`
* `source <(wget -O - https://raw.githubusercontent.com/peterkvt80/vbit2/master/getvbit2)`
* `Install service`
* „Choose new service to install“: `Custom`
* „Select type“: `git repo`
* „Enter URL“: `https://github.com/Luca090902/JvPeek-Teletext.git`
* „Enter name for service“: `JvPeek`
* „Is this a main or ancillary service?“: [< Main >]
* [Start VBIT2]
