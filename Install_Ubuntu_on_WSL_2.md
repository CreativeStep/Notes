##Install Ubuntu on WSL 2

WSL2 (Windows Subsystem for Linux 2) is a compatibility layer allowing users to run a full Linux kernel and native Linux applications on Windows 10 version 2004 and higher (Build 19041 and higher) or Windows 11.

### Install WSL command

1. Run PowerShell or Command Prompt as **administrator**
    
2. Run the “wsl —install” command to install. This will install default version of WSL.
    
    ```bash
    >wsl --install
    ```
    
3. Restart PC
    
4. Check wsl Installation
    
    ```bash
    >wsl --version
    WSL version: 2.2.4.0
    ....
    ```
    
5. Check installed Ubuntu with command “wsl --list --verbose” (or wsl -l -v).
    
    ```bash
    >wsl -l -v
      NAME                   STATE           VERSION
      Ubuntu                 Stopped         2
    ```
    
6. Enter Ubuntu Distribution.
    
    ```bash
    >wsl -d Ubuntu
    root@DESKTOP-FMBB4IH:/mnt/c/WINDOWS/system32#
    ```
    
7. Check the installed Ubuntu version.
    
    ```bash
    root@DESKTOP-FMBB4IH:/mnt/c/WINDOWS/system32#lsb_release -a
    No LSB modules are available.
    Distributor ID: Ubuntu
    Description:    Ubuntu 22.04.3 LTS
    Release:        22.04
    Codename:       jammy
    ```
    

### Change the installed default Linux distribution

1. To check the version of default Linux distribution
    
    Check the above “Install WSL command” procedure numbers 5, 6, and 7.
    
2. Check available distribution name using command wsl --list --online(wsl -l -o).
    
    ```bash
    >wsl -l -o
    Install using 'wsl.exe --install <Distro>'.
    
    NAME                            FRIENDLY NAME
    Ubuntu                          Ubuntu
    Debian                          Debian GNU/Linux
    kali-linux                      Kali Linux Rolling
    Ubuntu-18.04                    Ubuntu 18.04 LTS
    Ubuntu-20.04                    Ubuntu 20.04 LTS
    Ubuntu-22.04                    Ubuntu 22.04 LTS
    Ubuntu-24.04                    Ubuntu 24.04 LTS
    OracleLinux_7_9                 Oracle Linux 7.9
    OracleLinux_8_7                 Oracle Linux 8.7
    OracleLinux_9_1                 Oracle Linux 9.1
    openSUSE-Leap-15.6              openSUSE Leap 15.6
    SUSE-Linux-Enterprise-15-SP5    SUSE Linux Enterprise 15 SP5
    SUSE-Linux-Enterprise-15-SP6    SUSE Linux Enterprise 15 SP6
    openSUSE-Tumbleweed             openSUSE Tumbleweed
    ```
    
3. To change the installed default Linux distribution to Ubuntu-22.04.
    
    Syntax: wsl --install -d &lt;Distribution Name&gt;
    
    ```bash
    >wsl --install -d Ubuntu-24.04
    Installing: Ubuntu 24.04 LTS
    Ubuntu 24.04 LTS has been installed.
    Launching Ubuntu 24.04 LTS...
    Installing, this may take a few minutes...
    Please create a default UNIX user account. The username does not need to match your Windows username.
    For more information visit: https://aka.ms/wslusers
    Enter new UNIX username:
    ```
    
    Enter username and password 2 times when prompted.
    
4. Changed distribution is ready to use.
    
    Check the above “Install WSL command” procedure numbers 5, 6, and 7.
    
5. To enter the distribution
    
    Just after installation or changing the distribution, the distribution is opened. To open the distribution from next time, enter the following command:
    
    Syntax: wsl -d &lt;Distribution Name&gt;
    
    ```bash
    >wsl -d Ubuntu-24.04
    ```
    
6. To exit the distribution
    
    ```bash
    >exit
    ```
    
7. To uninstall the distribution
    
    Syntax: wsl —unregister &lt;Distribution Name&gt;
    
    ```bash
    >wsl --unregister Ubuntu-24.04
    ```
    

### Reference

1. [Windows Subsystem for Linux Documentation](https://learn.microsoft.com/en-us/windows/wsl/)