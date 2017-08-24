Role Name
=========

This role sets up systemd enabled system to router using systemd-networkd.

Requirements
------------

This role requires systemd, systemd-networkd and at least two network interfaces (LAN and WAN).

Role Variables
--------------

| Variable                | Default value      | Comments (type)                                       |
| :---                    | :---               | :---                                                  |
| `router_wan_int_name`   | `eth0`             | WAN Interface name (as seen on `ip a` command output  |
| `router_wan_ip_static`  | `false`            | false = DHCP, true is obvious (not implemented yet)   |
| `router_wan_ip_address` | `192.168.0.1/24`   | WAN IP address (not implemented yet)                  |
| `router_lan_int_name`   | `eth1`             | LAN Interface name (as seen on `ip a` command output) |
| `router_lan_ip_address` | `192.168.1.1/24`   | LAN IP address (quite self-explanatory, right?)       |
#| `` | `` | |

Dependencies
------------

None. Hopefully.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: ansible-router }

License
-------

GPLv3
