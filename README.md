# Deskmini-110-hackintosh

Deskmini110/COM hackintosh profile.

### Hardware

CPU: i5-7600T

Storage: Toshiba RD500 NVME SSD

Wi-Fi and bluetooth card: None

Both opencore and clover are supported, the latest system tested is Catalina 10.15.2.

### What will work

* 4k display support **on DP port**
* Audio 
* USB
* Ethernet
* Other trivial system functions

### What have not been tested

* Sleep 
* HDMI 

# Warning

I have tested them on my build. However, specific hardware differs, I do not guarantee these EFI will boot system successfully in every build, use them at your own risk.

### Usage

Please follow [ this guide ](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/) to start a clean catalina install and replace EFI folder with opencore or clover EFI in this repository.

Catalina and Mojave are different in many aspects, these EFI are not tested under Mojave. Please do not use them for Mojave in case of any problem like boot failure.

### Others

The EFI here **doesn't contain** any kext for Wi-Fi and bluetooth cards and SMBIOS information. Please find suitable kexts for Wi-Fi cards to work and generate your own valid SMBIOS to be able to use iMessage and FaceTime.

### Some explanations

Maybe you have noticed that I'm using a spoof ig-platform-id 0x19120000 of SkyLake rather than 0x59120000 to boot Kabylake Intel HD630, since a normal patch is able to boot into system but will have a random black out problem on 4k monitors on my build. A spoof id will make **HEVC support** unvaliable in video editing software such as VideoProc, it's not a final solution, but no better methods could be found at this time. 

