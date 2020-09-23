# Deskmini-110-hackintosh

Deskmini110/COM hackintosh EFI profile, Thanks to [dortania opencore tutorial](https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html#prerequisites).

### Hardware

CPU: i5-7600T

Storage: Toshiba RD500 NVME SSD

Wi-Fi and bluetooth card: None

Both opencore and clover are supported, the latest system tested is Catalina 10.15.2.

**Update**: Opencore 060 has been updated, GUI boot device selector, USB mapping, nvme fix and lots of patches are added, the lastest system tested is Catalina 10.15.6.

### What will work

* 4k display support **on DP port**
* Audio 
* USB
* Ethernet
* **Sleep**
* Other trivial system functions

### What have not been tested

* HDMI 
* VGA
* Airdrop (In theory, it will work if you insert Apple original cards since all the kexts needed are present here)

# Warning

I have tested them on my build. However, specific hardware differs, I do not guarantee these EFI will boot system successfully in every build, please use them at your own risk.

### Usage

Please follow [ this guide ](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/) to start a clean catalina install and replace EFI folder with opencore or clover EFI in this repository.

Catalina and Mojave are different in many aspects, these EFI are not tested under Mojave. Please do not use them for Mojave in case of any problem like boot failure.

### Others

The EFI here **doesn't contain**  SMBIOS information. Please generate your own valid SMBIOS to be able to use iMessage and FaceTime, [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) is recommended.

### Some explanations

Maybe you have noticed that I'm using a spoof ig-platform-id 0x19120000 of SkyLake rather than 0x59120000 to boot Kabylake Intel HD630, since a normal patch is able to boot into system but will have a random black out problem on 4k monitors on my build. A spoof id will make **HEVC support** unvaliable in video editing software such as VideoProc, it's not a final solution, but no better methods could be found at this time. 

