ansible-role-network
====================

Ansible role for network configuration

# Notes
!!! This role need a modification for the modprobe module available here : https://github.com/jdauphant/ansible/blob/devel/library/system/modprobe !!!

# Compatible
- Debian family

# Example :
```
# Create 3 dummy interface and assignate ip
network_dummies:
   - { address: 192.168.130.2, network: 255.255.255.255 }
   - { address: 192.168.130.3, network: 255.255.255.255 }
   - { address: 192.168.130.4, network: 255.255.255.255 }
```

