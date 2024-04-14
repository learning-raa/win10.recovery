# WinRE

### https://www.reddit.com/r/ZephyrusG14/comments/o4tteb/asus_winre_after_clean_install/
- `diskpart`
  - `> list vol`
  - `> sel vol #`
  - `> assign letter=C`
- `E:\Recovery\RecoveryImage\ASUS.swm`
  - `dism /apply-image /imagefile:E:\Recovery\RecoveryImage\ASUS.swm /index:1 /applydir:C:\`
- `bcdboot C:\Windows`
- `bcdedit ???`

### https://www.reddit.com/r/ZephyrusG15/comments/rn75ps/create_bootable_usb_from_recovery_partition/
- https://www.tenforums.com/tutorials/103340-dism-split-install-wim-file.html
- https://www.tenforums.com/tutorials/95941-diskpart-how-partition-gpt-disk.html

---

# Linux
(apt intall wimtools)
- `mkfs.ntfs /dev/sda2 -f -L OS`
- `wimapply install.wim 1 /dev/sda2 [--check --strict-acls]`

# PowerShell cleaner
- `Get-AppxPackage | Select Name,PackageFullName`
- `Get-AppxProvisionedPackage -online | Remove-AppxProvisionedPackage –online`
- `Get-AppxPackage -allusers *XXXX* | Remove-AppxPackage
  - .YourPhone
  - .Getstarted
  - .GetHelp
  - .GamingServices
  - .MixedReality
  - .GamingApp
  - .Microsoft3DViewer
  - .Messaging
  - .BingWeather
  - .Windows.Photos
  - .Wallet
  - .WindowsCamera
  - .WindowsFeedBackHub
  - .ZuneVideo
  - .ZuneMusic
  - .People
  - .Office.OneNote
  - .MicrocoftOfficeHub
  - .WindowsMaps
  - .WindowsSoundRecorder
  - .WebpImageExtension
  - .SkypeApp
  - .DolbyAccess
  - .MicrosoftEEdge.Beta
  - .WindowsAlarms
  - .MicrosoftSolitaireCollection
  - 
