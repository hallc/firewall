# Firewall
A simple iptables firewall that blocks incoming connections.

## Installing
Drop `firewall` in `/etc/init.d` and configure it to start automatically.  Instructions will vary depending on your distribution, but the script includes headers for `chkconfig` and [LSB Init Scripts](https://wiki.debian.org/LSBInitScripts).

## Allowing ICMP & SSH
To allow ICMP traffic (ping, traceroute, etc), uncomment line 32:

`#iptables -A INPUT -p icmp -j ACCEPT`

To allow SSH traffic, uncomment line 35:

`#iptables -A INPUT -p tcp --dport 22 -m state --state NEW -j ACCEPT`

## License
This script is distributed under the MIT license.

