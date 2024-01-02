## What is TorGhost ?
TorGhost is an anonymization script. TorGhost redirects all internet traffic through SOCKS5 tor proxy. DNS requests are also redirected via tor, thus preventing DNSLeak. The scripts also disables unsafe packets exiting the system. Some packets like ping request can compromise your identity.

This version is optimized for the usage with **Kali Linux Rolling**: 6.5.0-kali3-amd64 
Get it from: https://www.kali.org/get-kali/#kali-platforms

It is a fork from the original TorGhost by SusmithKrishnan: https://github.com/SusmithKrishnan/torghost.git

## Build and install from source
Open a terminal (you will start in the home folder: **/home/kali**) and type:

`git clone https://github.com/siegfriedbolz/torghost`

`cd torghost`

`chmod +x torghost.py`

`sudo python3 torghost.py`

You will see a confirmation screen.

## Start TorGhost
`sudo python3 torghost.py -s`

## Stop TorGhost
`sudo python3 torghost.py -x`

## Check that it is working correctly
Visit page: https://check.torproject.org/

## Usage
Torghost v3.0 usage:

`  -s      --start        Start Torghost`

`  -r      --switch       Request new tor exit node`

`  -x      --stop         Stop Torghost`

`  -h      --help         Print this help and exit`

`  -u      --update       Checks for updates`

## Terminal shortcuts for later usage:
`sudo python3 ~/torghost/torghost.py -s`

`sudo python3 ~/torghost/torghost.py -x`

## Create a desktop shortcut
Open a terminal and type:
```
cd ~/Desktop
sudo nano torghost.desktop
```


Insert this into the file:
```
[Desktop Entry]
Version=1.0
Type=Application
Terminal=true
Exec=sudo python3 /home/kali/torghost/torghost.py -s
Name=TorGhost
Comment=Start TorGhost
Icon=network-workgroup
```

Save it with **CTRL+O** and exit with **CTRL+X**.
An icon will appear on your desktop. Double click it to start TorGhost.
