Welcome to the console-server wiki!

# console-server
Building a multi-purpose Raspberry Pi console server with strict mapping of USB ports and network troubleshooting tools.

Requirements:
* Raspberry Pi with Jessie
* USB cables

1. Update the Raspberry Pi to the latest packages

    `sudo apt-get update && sudo apt-get upgrade && sudo rpi-update`

    Reboot the system

2. Install nice-to-have tools

    `sudo apt-get install tshark tcpdump wireshark nmap minicom ser2net`

3. Configure remote-access services

    `sudo raspi-config`
    *  1 Change User Password
    *  2 Hostname   
    *  3 Boot Options > B1 Desktop / CLI > B1 Console
    *  5 Interfacing Options > P3 VNC
    *  7 Advanced Options > A1 Expand Filesystem 

    Reboot the system

4. Map physical USB ports to strict logical devices

   `Copy 88-oobm.rules file to /etc/udev/rules.d/`

5. Configure ser2net
    copy ser2net.conf to /etc/ser2net/ser2net.conf

6. Set static IP addresses on eth0

    `interface eth0`

    `static ip_address=172.17.x.5/24`

    `static routers=172.17.x.1`

    `static domain_name_servers=8.8.8.8`
