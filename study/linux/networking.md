## Network

### Interface Configuration

`vi /etc/network/interfaces`

Example static IP:

```
auto eth0
iface eth0 inet static
address 192.168.0.2
netmask 255.255.255.248
gateway 192.168.0.1 

auto eth0:0
iface eth0:0 inet static
address 192.168.0.3
netmask 255.255.255.248
gateway 192.168.0.1 

auto eth0:1
iface eth0:1 inet static
address 192.168.0.4
netmask 255.255.255.248
gateway 192.168.0.1
```

To restart the network:

`/etc/init.d/networking restart`

### DHCP

How to change domain returned from DHCP.

```
vi /etc/dhcp/dhclient.conf
supersede domain-name "fugue.com home.vix.com";

cat /var/lib/dhcp/dhclient.eth0.leases
```
