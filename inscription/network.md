# Network

We use 2 Ubiquiti Rocket M2 for wireless network between the base station and the rover.
By default (or after factory reset), the device IP address will be 192.168.1.20.
It won't serve as DHCP server, therefore, we need to set the computer to a static IP address.
Then open 192.168.1.20 on the browser to changing configurations.
The default username and password are `uqnt`.
As there are two devices, we need to change IP address of one of them.
The recommendation is changing the base station one.

1. Changing IP address to avoid IP duplication.
2. Changing mode of operation from `bridge` to `access point`.
