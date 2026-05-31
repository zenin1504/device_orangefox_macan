# Ace 6T (PLR110) Android device tree

## Status

- [X] Display
- [X] MTP/OTG Storage
- [X] ADB/Fastbootd
- [] Vibrator
- [X] Display Settings
- [X] Flashing 
- [X] Backup & Restore 
- [X] Factory Reset
- [X] Touch
- [X] Decryption
- [] Flashlight

# Building

### Clone & sync source
```
mkdir -p ~/OrangeFox_14
cd ~/OrangeFox_14
git clone https://gitlab.com/OrangeFox/sync.git
cd sync
./orangefox_sync.sh --branch 14.1 --path ~/fox_14.1
```
### Clone device tree
```
cd ~/fox_14.1
git clone https://github.com/zenin1504/device_oneplus_macan.git -b 14.1 device/oneplus/macan
```
### BUILD
```
cd ~/fox_14.1
source build/envsetup.sh
lunch twrp_macan-ap2a-eng
mka adbd recoveryimage
```
