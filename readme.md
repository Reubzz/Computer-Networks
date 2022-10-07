# Computer Network Practicals

| Table of Contents |
| :--: |
| [Static Routing](#static-routing) |
| [RIP Routing](#rip-routing) |
| [OSPF Routing (Single Area)](#ospf-routing-single-area) |
| [OSPF Routing (Multi Area)](#ospf-routing-multi-area) |
| [DHCP Server](#dhcp-routing) |
| [DNS Server](#dns-routing) |

## Static Routing

### Base Command - `ip route <destination_network> <subnet_mask> <next_hop_Address>`

where: 
- `<destination_network>` => The network Address of the link connected recieving PC. It must end in a `0`. eg: (192.168.0.0)
- `subnet_mask` => The Subnet mask of the `<destination_network>`
- `Next_Hop_Address` => The Address of the recieving end of the router.

In below Example, If setting up Static Routing for Left Router (R1) the command would be following: 
```md
Router> en
Router# conf t
Router(config)# ip route 10.0.0.0 255.0.0.0 192.168.0.2
```

<img src="./Assets/Static Routing.png" width="500px"></img>

### RIP Routing

### Base Command - `router rip`, `network <network_address>`

where: 
- `<network_address>` => The networks the current router is connected to. It must end in a `0`. eg: (172.16.0.0).

Example, if setting up RIP Routing for Top Left Router (R1) the Commands would be as follows:
```md
Router> en
Router# conf t
Router(config)# router rip
Router(config-router)# network 192.168.1.0
Router(config-router)# network 172.32.1.0
Router(config-router)# network 128.0.0.1
exit
```

### OSPF Routing (Single Area)


### OSPF Routing (Multi Area)
### DHCP Routing
### DNS Routing