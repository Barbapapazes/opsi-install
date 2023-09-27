# opsi-install

[To install Opsi](https://docs.opsi.org/opsi-docs-en/4.2/index.html)

## Packages

Use opsi-setup-detector to create opsiscript and opsi PackageBuilder to build packages.

- `Firefox`, use https://www.mozilla.org/en-US/firefox/enterprise, rename it `firefox_esr.exe` and move it into `firefox/CLIENT_DATA`
- `PuTTY`, use https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html (x64), rename it `putty-64bit-0.79-installer` and move it into `putty/CLIENT_DATA/files1`
- `LibreOffice`, use https://fr.libreoffice.org/download/telecharger-libreoffice/, rename it `LibreOffice_7.6.1_Win_x86-64` and move it into `libreoffice/CLIENT_DATA/files1`
- `Visual Studio Code`, use https://code.visualstudio.com/Download (System Installer x64), renamte it `VSCodeSetup-x64-1.82.2` and move it into `code/CLIENT_DATA/files1`
- `Wireshark`, use https://www.wireshark.org/ (Installer), rename it `Wireshark-win64-4.0.8` and move it into `wireshark/CLIENT_DATA/file1`
- `VMware Player`, use https://www.vmware.com/fr/products/workstation-player/workstation-player-evaluation.html, rename it `VMware-player-full-17.0.2-21581411` and move it into `vmware/CLIENT_DATA/files1`
- `Hyper-V`, use a PowerShell script to install it and to remove it.
- `Zabbix`, ask Monitoring for the MSI file, rename it `zabbix` and move it into `zabbix/CLIENT_DATA`

### Install Packages

```sh
# Run all of these commands inside the application folder
sudo opsi-makepackage --no-md5 --no-zsync
sudo opsi-set-rights .
sudo opsi-package-manager -v -i -S *.opsi
```
