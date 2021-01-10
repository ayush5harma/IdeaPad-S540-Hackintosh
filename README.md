# IdeaPad-S540-Hackintosh  
<p align="center">
  <img src="https://user-images.githubusercontent.com/47772616/104133915-8ffaf100-53ac-11eb-83f9-ed528b47670c.png" />
</p>

## Specifications :  

Device | Details | Status |
------------ | ------------- | ------------- | 
CPU | **Intel(R) Core(TM) i5-10210U CPU @ 1.60GHz** | Working |
Graphic | Intel UHD630 | Working |
WiFi | Intel Wireless-AC 9462 | Working |
Card Reader | Bayhub_1.1.101.1025 | Working |
Camera | Chicony-AVC_10.0.17763.20070 | Working |
Audio | 2X2W Dual Speaker, With Dolby Audio | Working |
Touchpad | Synaptics Trackpad | Working |
Discrete Graphic | Nvidia GeForce 250MX | Unsupported, Disabled by default |
Bios Version | CNCN16WW | Secure Boot Disabled |
HDMI |    | Working |
USB Ports |      | Working |
Fingerprint reader | Goodix| Disabled (recognised but can't be used) |
SSD | Samsung PM981  | R/W works with NVMeFix (however macOS install doesn't work) |
OS | BigSur | Working |

## Setting Up 

1. Place the EFI folder to the EFI partition

2. Generate your own SMBIOS :

- Do the following one line at a time in Terminal:
```
    git clone https://github.com/corpnewt/GenSMBIOS
    cd GenSMBIOS
    chmod +x GenSMBIOS.command
```
    
- Then run with either `python ./GenSMBIOS.command` on *nix system or by double-clicking *GenSMBIOS.command* on macOS.
On Windows `./GenSMBIOS.bat`.

- Choose *Install/Update MacSerial*.

- Then choose *Select the config.plist file* and select it from the EFI folder. 

- Now choose *Generate SMBIOS* and generate the SMBIOS by entering MacBookPro16,1

3. Finalising with proper tree:  

#### On *nix systems:

```
git clone https://github.com/corpnewt/ProperTree
python ./ProperTree/ProperTree.command
```

\* On macOS, you can simply double-click the `ProperTree.command` after cloning to launch.

#### On Windows:

```
git clone https://github.com/corpnewt/ProperTree
./ProperTree/ProperTree.bat
```

- Press Ctrl + O and select config.plist   
- Press Ctrl + Shift + R and navigate to /EFI/OC/ and click open 
- Save the changes..
