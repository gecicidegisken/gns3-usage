## Cisco Routers


* [Usage](#usage)
    * [Getting Help](#getting-help)
    * [Configuration Mode](#configuration-mode)
    * [Interface Configuration Mode](#interface-configuration-mode)
    * [Show Configuration](#show)
* [DHCP Server](#dhcp-server)
* [NAT](#nat)
### Usage
After starting the router, you can open a console to manage and configure it and use the following commands to configure the router:

#### Getting Help
* `?`: Command shows a list of available commands.

#### Configuration Mode
*  `conf t` or `config t`: Enter terminal configuration mode
* `interface <interface>` or `int <interface>`: Enter interface configuration mode
* `exit`: Exit from the current mode

#### Interface Configuration Mode
* `ip address <ip address> <subnet mask>`: Set the IP address of the interface
* `no shutdown`: Enable the interface
* `shutdown`: Disable the interface

#### Show 
Remember that you can use show commands in default mode.

* `show ip interface brief`: Show a summary of the IP addresses of the interfaces. Can be abbreviated to `show ip int br`
* `show ip interface <interface>`: Show detailed information about the IP address of the interface. Can be abbreviated to `show ip int <interface>`
* `show ip route`: Show the routing table
* `show ip arp`: Show the ARP table. Can be abbreviated to `show arp`
* `show ip dhcp pool`: Show the DHCP pools 

### DHCP Server
* `ip dhcp pool <pool name>`: Create a DHCP pool
* `network <network address> <subnet mask>`: Set the network address of the DHCP pool
* `default-router <ip address>`: Set the default gateway of the DHCP pool
* `dns-server <ip address>`: Set the DNS server of the DHCP pool

### NAT

#### Static NAT
* R(interface)`ip nat inside` : Configure interface as NAT inside interface
* `ip nat outside`: Configure interface as NAT outside interface
* `ip nat inside source static <source-ip> <dest-ip>` : Configure a static NAT translation

#### Dynamic NAT
* `access-list 1 permit <ip-address> <subnet-mask>`:  Permit traffic from <ip-address>
* `ip nat pool <pool-name> <start-ip-addr> <end-ip-addr> netmask <netmask>`: #create a NAT pool
* `ip nat inside source list 1 pool <pool-name>` : Enable pool
   
