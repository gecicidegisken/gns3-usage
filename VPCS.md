## VPCS
Virtual PC Simulator (VPCS) is a simple virtual PC that can be used to simulate a PC in a network.

### Usage
After starting VPCS, you can open a console to manage and configure it and use the following commands to configure the PC:

#### Getting Help
* `?`: Command shows a list of available commands. You can add a command name to get help on a specific command. For example, `ip ?` will show help on the `ip` command.


#### IP Address

* `ip <ip address>`: Set the IP address of the PC manually

    #### DHCP
    * `ip dhcp` or `dhcp`: Set the IP address of the PC via DHCP 

### Show
* `show`: Show summary information like IP address, MAC address, gateway, etc.
* `show ip`: Show detailed information about the IP address
* `show arp`: Show the ARP table of the PC


### Ping
* `ping <ip address>`: Send an ICMP echo request to the specified IP address
