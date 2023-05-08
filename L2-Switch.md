## L2 Switch
This document refers to IOSv-L2 switch.

<!-- table of contents -->
* [Usage](#usage)
    * [Getting Help](#getting-help)
    * [Configuration Mode](#configuration-mode)
    * [Show Configuration](#show-configuration)
* [VLAN](#vlan)
    * [Access Port](#access-port)
    * [Trunk Port](#trunk-port)


### Usage
After starting the switch, you can open a console to manage and configure it and use the following commands to configure the switch:

#### Getting Help
* `?`: Command shows a list of available commands. You can add a command name to get help on a specific command.

#### Configuration Mode
* `sh enable`: Enter privileged mode. **This is required to configure the switch.**
* `conf t`: Enter terminal configuration mode
* `interface <interface>`: Enter interface configuration mode
* `exit`: Exit from the current mode

#### Show Configuration

* `show interfaces`: Show interfaces
* `show interfaces status`: Show interface statuses
* `show interfaces description`: Show interface descriptions
* `show interfaces <interface>`: Show detailed information about the interface

### VLAN
* `vlan <vlan-id>`: Create a VLAN. VLAN ID must be between 1 and 4094. Enters VLAN configuration mode.
* `name <name>`: Set the name of the VLAN.
* `show vlan`: Show VLANs
* `show interfaces switchport`: Show switchport configuration

    #### Access Port
    Run the following commands in interface configuration mode to configure an access port:
    * `switchport mode access`: Configure interface as access port
    * `switchport access vlan <vlan-id>`: Assign the access port a VLAN

    #### Trunk Port
    Run the following commands in interface configuration mode to configure a trunk port:
    * `switchport trunk encapsulation dot1q`: Configure trunk encapsulation as 802.1Q
    * `switchport mode trunk`: Configure interface as trunk port
    * `switchport trunk allowed vlan <vlan-id>`: Assign allowed VLANs to the trunk port
  
  
 ### STP
 * `spanning-tree vlan 1` : Enable STP for VLAN 1
 * `show spanning-tree`: Show STP configurations
 * `spanning-tree priority <value>`: Change switch priority value
 * `spanning-tree vlan 1 root primary`: Set switch as primary root bridge
 * `clear spanning-tree [interface]`: Clear STP for an interface
 * `spanning-tree port-priority [interface] [priority]` : Set priority for an interfaceü
 * `no spanning-tree vlan 1` : Disable STP for VLAN 1
 
    

