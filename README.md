ansible-role-network
====================

Ansible role for network configuration

# Notes
!!! This role is **dangerous** you can lost the connection with the server.
!!! This role need a modification for the modprobe module available here : https://github.com/jdauphant/ansible/blob/devel/library/system/modprobe !!!


# Support
- Dummies interfaces

# Compatible
- Debian family

# Example :
```
# Configure eth0 with dhcp and eth1 with static
network_interfaces:
     -  name: "eth0"
        type: "dhcp"
     -  name: "eth1"
        type: "static"
        address: "192.168.0.20"
        netmask: "255.255.255.0"
        gateway: "192.168.0.1"
        dns: ["192.168.1.10","192.168.2.10"]

# Create 3 dummy interface and assignate ip
network_dummies:
   - { address: 192.168.130.2, network: 255.255.255.255 }
   - { address: 192.168.130.3, network: 255.255.255.255 }
   - { address: 192.168.130.4, network: 255.255.255.255 }

# Disable interface
network_interfaces_disabled: ['eth3','eth4']

```

