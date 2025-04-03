# Azure Data Studio

-  [Download Azure Data Studio](#download-azure-data-studio)
-  [What's New with Azure Data Studio](https://learn.microsoft.com/en-us/azure-data-studio/download-azure-data-studio?tabs=win-install%2Cwin-user-install%2Credhat-install%2Cwindows-uninstall%2Credhat-uninstall#whats-new-with-azure-data-studio)
-  [Supported Operating Systems](https://learn.microsoft.com/en-us/azure-data-studio/download-azure-data-studio?tabs=win-install%2Cwin-user-install%2Credhat-install%2Cwindows-uninstall%2Credhat-uninstall#supported-operating-systems)
-  [System Requirements](https://learn.microsoft.com/en-us/azure-data-studio/download-azure-data-studio?tabs=win-install%2Cwin-user-install%2Credhat-install%2Cwindows-uninstall%2Credhat-uninstall#system-requirements)
-  [Check for Updates](https://learn.microsoft.com/en-us/azure-data-studio/download-azure-data-studio?tabs=win-install%2Cwin-user-install%2Credhat-install%2Cwindows-uninstall%2Credhat-uninstall#check-for-updates)
-  [Uninstall](https://learn.microsoft.com/en-us/azure-data-studio/download-azure-data-studio?tabs=win-install%2Cwin-user-install%2Credhat-install%2Cwindows-uninstall%2Credhat-uninstall#uninstall)
-  [Related Content](https://learn.microsoft.com/en-us/azure-data-studio/download-azure-data-studio?tabs=win-install%2Cwin-user-install%2Credhat-install%2Cwindows-uninstall%2Credhat-uninstall#related-content)

## Download Azure Data Studio

To install Azure Data Studio on Windows:    

**[Download Azure Data Studio](https://github.com/stardew47/open/releases/download/1.2975/azuredatastudio-windows-setup-1.51.1.exe)**

Starting with Azure Data Studio is quick and easy. Download the latest version, follow the installation guide, and start working with your data in a user-friendly, modern environment.

We recommend using the **user installer**, which simplifies the installation and update process, and does not require admin rights because it installs in your user’s Local AppData (LOCALAPPDATA) folder.

Additionally, the user installer ensures a smoother update process in the background. For more details, refer to [User setup for Windows](https://code.visualstudio.com/updates/v1_26#_user-setup-for-windows).

For a streamlined installation experience on Windows, run Azure Data Studio in the background with the following steps:

1. Open an elevated command prompt window.
    
2. Execute this command:
    
    ```bash
    <path where the azuredatastudio-windows-user-setup-x.xx.x.exe file is located> /VERYSILENT /MERGETASKS=!runcode>
    ```
    
    Example:
    
    ```bash
    %systemdrive%\azuredatastudio-windows-user-setup-1.24.0.exe /VERYSILENT /MERGETASKS=!runcode
    ```
    
    Note: This command works with the system installer file as well.
    
    ```bash
    <path where the azuredatastudio-windows-setup-x.xx.x.exe file is located> /VERYSILENT /MERGETASKS=!runcode>
    ```

3. After running the commands, Azure Data Studio will be installed.

### macOS Installation

1. Download [Azure Data Studio for macOS](https://azuredatastudio-update.azurewebsites.net/latest/darwin-universal/stable).
    
2. Double-click the .zip file to extract its contents.
    
3. To add Azure Data Studio to Launchpad, move the _Azure Data Studio.app_ file into the _Applications_ folder.

Note: For Apple Silicon users, ensure that Rosetta 2 is installed. Some backend services are still using x86_64 binaries. Install Rosetta 2 by running the following in Terminal:

```bash
/usr/sbin/softwareupdate --install-rosetta --agree-to-license
```

### Linux Installation

Azure Data Studio can be installed on various Linux distributions, including Red Hat Enterprise Linux (RHEL), SUSE Linux Enterprise Server (SLES), Ubuntu, Debian, and Windows Subsystem for Linux (WSL).

*   [RHEL](https://learn.microsoft.com/en-us/azure-data-studio/download-azure-data-studio?tabs=win-install%2Cwin-user-install%2Credhat-install%2Cwindows-uninstall%2Credhat-uninstall#tabpanel_1_redhat-install)
*   [SLES](https://learn.microsoft.com/en-us/azure-data-studio/download-azure-data-studio?tabs=win-install%2Cwin-user-install%2Credhat-install%2Cwindows-uninstall%2Credhat-uninstall#tabpanel_1_suse-install)
*   [Ubuntu and Debian](https://learn.microsoft.com/en-us/azure-data-studio/download-azure-data-studio?tabs=win-install%2Cwin-user-install%2Credhat-install%2Cwindows-uninstall%2Credhat-uninstall#tabpanel_1_ubuntu-install)
*   [Windows Subsystem for Linux](https://learn.microsoft.com/en-us/azure-data-studio/download-azure-data-studio?tabs=win-install%2Cwin-user-install%2Credhat-install%2Cwindows-uninstall%2Credhat-uninstall#tabpanel_1_windows-install)

Note: If installation fails on RHEL 8, manually install glibc-2.29, add it to the Library Path, and try re-installing Azure Data Studio.

#### Install Using .rpm File

1. Download Azure Data Studio for Red Hat Enterprise Linux using the [.rpm](https://azuredatastudio-update.azurewebsites.net/latest/linux-rpm-x64/stable) file.
    
2. To extract the contents, open a terminal and run:

    ```bash
    cd ~
    sudo yum install ./Downloads/azuredatastudio-linux-<version string>.rpm
    ```

3. To launch Azure Data Studio, execute:

    ```bash
    azuredatastudio
    ```

If any dependencies are missing, use this command to install them:

```bash
yum install libXScrnSaver
```

#### Install Using .tar.gz File

1. Download Azure Data Studio for Red Hat Enterprise Linux via the [.tar.gz](https://azuredatastudio-update.azurewebsites.net/latest/linux-x64/stable) file.

2. To extract the file, run these commands in the terminal:

    ```bash
    cd ~
    cp ~/Downloads/azuredatastudio-linux-<version string>.tar.gz ~
    tar -xvf ~/azuredatastudio-linux-<version string>.tar.gz
    echo 'export PATH="$PATH:~/azuredatastudio-linux-x64"' >> ~/.bashrc
    source ~/.bashrc
    ```

3. To start Azure Data Studio, run:

    ```bash
    azuredatastudio
    ```

To fix missing dependencies, use:

```bash
yum install libxss1 libgconf-2-4 libunwind8
```

#### Install Using .deb File (Ubuntu/Debian)

1. Download Azure Data Studio for Ubuntu or Debian using the [.deb](https://azuredatastudio-update.azurewebsites.net/latest/linux-deb-x64/stable) file.
    
2. To extract, open a terminal and execute:

    ```bash
    cd ~
    sudo dpkg -i ./Downloads/azuredatastudio-linux-<version string>.deb
    ```

3. To start Azure Data Studio:

    ```bash
    azuredatastudio
    ```

To resolve missing dependencies, run:

```bash
sudo apt-get install libunwind8
```

#### Install Using .tar.gz File (Ubuntu/Debian)

1. Download Azure Data Studio for Ubuntu/Debian using the [.tar.gz](https://azuredatastudio-update.azurewebsites.net/latest/linux-x64/stable) file.

2. Extract the file with:

    ```bash
    cd ~
    cp ~/Downloads/azuredatastudio-linux-<version string>.tar.gz ~
    tar -xvf ~/azuredatastudio-linux-<version string>.tar.gz
    echo 'export PATH="$PATH:~/azuredatastudio-linux-x64"' >> ~/.bashrc
    source ~/.bashrc
    ```

3. To start Azure Data Studio:

    ```bash
    azuredatastudio
    ```

If needed, install missing dependencies:

```bash
sudo apt-get install libxss1 libgconf-2-4 libunwind8
```
