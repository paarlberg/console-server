# console-server
Building a multi-purpose Raspberry Pi console server with strict mapping of USB ports and network troubleshooting tools.

Requirements:
* Raspberry Pi with Jessie
* USB cables

1. Update the Raspberry Pi to the latest packages
    sudo apt-get update && apt-get upgrade
    sudo rpi-update
2. Install nice-to-have tools
    sudo apt-get install tshark tcpdump wireshark nmap minicom
3. Configure remote-access services
4. Map physical USB ports to strict logical devices
5. Install ser2net package
6. Configure ser2net
7. Making ser2net start on boot
