# Lenovo-T460-Hackintosh-Big Sur-OpenCore
This repo contains the files and scripts to install macOS on the Lenovo T460 family.

# 2023 VENTURA 13.4 UPDATE
This new release allows for the installation of MacOS Ventura 13.4 on a Thinkpad T460.
This update was A PAIN IN THE ASS to get it to work properly. 
Some instructions:
1. Apple keeps messing with the bluetooth. So for 13.4 a patch in config.plist is necessary. DO NOT UPDATE to 13.5 because it breaks bluetooth again. Search first. 
2. I switched back to the stock Intel WiFi card. If you have a Broadcom card amend EFI. 
3. Install Thinkpad assistant app for full keyboard F keys functionality.
4. The fan seems to spin up more often than before. Haven' t played with VoltageShift yet.   

Fill in platfom info on config.plist

![alt text](https://github.com/Hasodikis/Lenovo-T460-OpenCore/blob/master/Photos/1611225483522.jpg?raw=true)


![alt text](https://github.com/Hasodikis/Lenovo-T460-OpenCore/blob/master/Photos/Screen%20Shot%202021-01-21%20at%2012.35.54%20PM.png?raw=true)

# Laptop's Hardware
- <b>Model</b>: Thinkpad T460 (20FN003LGE)
- <b>Bios</b>: 1.42
- <b>CPU</b>: Intel(R) Core(TM) i5-6200U CPU @ 2.30GHz
- <b>GPU</b>: Intel HD Graphics 520
- <b>Storage</b>: Samsung 256 BG SSD
- <b>RAM</b>: 8 GB PC3L-12800 1600MHz DDR3L
- <b>Screen</b>: 14" FHD (1920x1080) IPS
- <b>Wi-Fi</b>: Broadcom BCM43xx
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

# Cosmetics - Mods - ETC

- I suggest to all of you to use Voltageshift for undervolting and maximum energy efficiency. Go to https://github.com/sicreative/VoltageShift and download it. The best way to use it (in my oppinion) is to load the kext form the EFI. Place the VoltageShift.kext in EFI/OC/kexts and load it with config.plist. Have a copy of the kext and the executable in a folder on your disk. Right now I am working stably with:
CPU voltage offset: -80mv
GPU voltage offset: -80mv
CPU Cache voltage offset: -60mv

- I replaced the German layout keyboard with a backlid US qwerty one. Its a cheap and easy replacement. 

- One of the main design/construction flaws, in my oppinion, with this laptop is the contact between the screen panel and the keyborad, when the laptop is carried in tight scpaces (backpacks etc). This can cause permanent scratches on the screen surface. To avoid that i suggest you use a screen protector. There are plenty in ebay and its a cheap mod. 

- Although the intel wifi card that came with the laptop works, Its more or less unstable and has several issues (slow boot, slower speeds, drops, problems after sleep  etc). I suggest you replace the original wifi card with something more compatible.  

