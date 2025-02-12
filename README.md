# winbox-linux
A simple helper script to install Mikrotik's Winbox in GNU/Linux

## Feature:
1. Supported GNU/Linux distributtions: Debian, Ubuntu, Elementary OS, Zorin OS, Linux Mint, Kali Linux, Fedora, RHEL, CentOS, IGOS Nusantara, Archlinux
2. Installs wine
3. Upgrades wine (from the distribution's repo) to a newer version (only for Fedora, RHEL, CentOS, IGN)
4. Menu entry in the application launcher
5. Latest winbox from https://mikrotik.com/download
6. Supports launch from terminal

## How to install:
Copy and paste this into your terminal::

```
cd /tmp && \
git clone https://github.com/mukhumaev/winbox-linux.git && \
cd winbox-linux && \
sudo ./winbox-linux install 
```

## How to remove:
If you want to remove winbox, just run this command:

`sudo ./winbox-linux uninstall`

## Supported ENV's:
You can change the behavior of the script by setting the environment parameters:
```
DEPENDS_PACKAGES                      List of dependencies
                                        Example: 'wine wget'

DESKTOP_FILE                          Linux '.desktop' file location
                                        Example: '/usr/share/applications/winbox.desktop'

WINBOX_EXE                            Winbox executable file location
                                        Example: '/usr/local/bin/winbox64.exe'

URL_WINBOX                            URL to download '/usr/local/bin/winbox64.exe' file
                                        Example: 'https://mt.lv/winbox64'

EXEC_FILE                             Location to store winbox run script
                                        Example: '/usr/local/bin/winbox'
```

## Firewall setting:
On Fedora/CentOS/Redhat, if you experience neighbor discovery problems, open the port in the firewall

`firewall-cmd --permanent --add-port=5678/udp`

`firewall-cmd --reload`

## Run from terminal
After installing winbox, you can run it through the terminal:
`winbox [HOST] [USERNAME] [PASSWORD]`

Example:
`winbox 192.168.88.1 admin super-password`
