# win10.recovery


### https://www.reddit.com/r/ZephyrusG14/comments/o4tteb/asus_winre_after_clean_install/
- `diskpart`
  - `> list vol`
  - `> sel vol #`
  - `> assign letter=C`
- `..Recovery\RecoveryPackage\ASUS.swm`
  - `dism /apply-image /imagefile:path/to/ASUS.swm /index:1 /applydir:C:\`
- `bcdboot C:\Windows`
- `bcdedit ???`
