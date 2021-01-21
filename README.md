# Lenovo-T460-Hackintosh-Big Sur-OpenCore
This repo contains the files and scripts to install macOS on the Lenovo T460 family
This set up is based on OpenCore 0.6.5 and it uses the Intel Wireless -AC 8260 that came with the laptop

Due to file size limitations I am posting the Recourses folder seperately. Just paste it inside OC folder.

# Laptop's Hardware
- <b>Model</b>: Thinkpad T460 (20FN003LGE)
- <b>Bios</b>: 1.42
- <b>CPU</b>: Intel(R) Core(TM) i5-6200U CPU @ 2.30GHz
- <b>GPU</b>: Intel HD Graphics 520
- <b>Storage</b>: Samsung 256 BG SSD
- <b>RAM</b>: 8 GB PC3L-12800 1600MHz DDR3L
- <b>Screen</b>: 14" FHD (1920x1080) IPS
- <b>Wi-Fi</b>: Intel Wireless - AC 8260
- <b>Ethernet</b>: Intel I219-V PCIe Gigabit Ethernet
- <b>Sound</b>: Realtek ALC3245 (same as ALC239)
- <b>Camera</b>: 720p
- <b>Battery</b>: 3-cell (23Wh) + 3-cell (23Wh)

# Bios settings

<b>Security</b>
- `Security Chip` **Disabled**
- `Memory Protection -> Execution Prevention` **Enabled**
- `Virtualization -> Intel Virtualization Technology` **Enabled**
- `Virtualization -> Intel VT-d Feature` **Enabled**
- `Anti-Theft -> Computrace -> Current Setting` **Disabled**
- `Secure Boot -> Secure Boot` **Disabled**
- `Intel SGX -> Intel SGX Control` **Disabled**
- `Device Guard` **Disabled**

<b>Startup</b>
- `UEFI/Legacy Boot` **UEFI Only**
- `CSM Support` **No**

# What's Working?
- [x] Intel HD 520 Graphics (incuding graphics acceleration)
- [x] CPU Power Management
- [x] Battery
- [x] All USB ports
- [x] HDMI port (including HDMI Audio)
- [x] Intel I219V Ethernet port
- [x] Realtek ALC239 Audio (including headphones jack)
- [x] Wi-Fi & Bluetooth (including Apple services)
- [x] Internal camera (including Facetime)
- [x] Trackpad, Trackpoint and physical buttons (including gestures)
- [x] Sleep / Wake / Shutdown / Reboot (lid sleep and lid wake)
- [x] Keyboard (incuding all fn Keys using [ThinkpadAssistant](https://github.com/MSzturc/ThinkpadAssistant))
- [x] iMessage, FaceTime, App Store, iTunes Store (with valid smbios)
- [x] DRM support (iTunes Movies, Apple TV+, Amazon Prime and Netflix, and others)
- [x] SD Card Reader (v2.2 works but still a bit unstable)

# What's not working ⚠️
- [ ] Fingerprint Reader (will never work since no drivers available)
- [ ] Sidecar Wireless (doesn't work without apple native WIFI card)
