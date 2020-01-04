# Deskmini-110-hackintosh

Deskmini110/COM hackintosh profile.

CPU: i5-7600T
Storage: Toshiba RD500
Wi-Fi and bluetooth card: None

Both opencore and clover are supported, the latest system tested is Catalina 10.15.2.

### Warning: I have tested them on my build without problem. However, specific hardware differs, use it at your own risk.

### Usage

Please follow [ this guide ](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/) to start a clean catalina install and replace EFI folder with opencore or clover EFI in this repository.

I have not tested them under Mojave so please do not use them for Mojave to avoid any boot failure problem.

### Others
The EFI here **doesn't contain** any kext for Wi-Fi and bluetooth cards and SMBIOS information. Please find suitable kexts for Wi-Fi cards and generate your own SMBIOS to be able to use iMessage.

### Some explanations

Maybe you have noticed that I'm using a spoof ig-platform-id 0x19120000 of SkyLake rather than 0x59120000 to boot Kabylake Intel HD630, since a normal patch is able to boot into system but will have a random black out problem on 4k monitors on my build. A spoof id will make HEVC support unvaliable in software such as VideoProc, it's not a final solution, but no better method could be found.
