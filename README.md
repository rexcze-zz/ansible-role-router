Router
=========

[![Build Status](https://travis-ci.org/rexcze/ansible-role-router.svg?branch=master)](https://travis-ci.org/rexcze/ansible-role-router)

This role sets up systemd enabled system to router using systemd-networkd.

Requirements
------------

This role requires systemd, systemd-networkd and at least two network interfaces (LAN and WAN).

Role Variables
--------------

| Variable                        | Default value      | Comments (type)                                       |
| :---                            | :---               | :---                                                  |
| `router_wan_int_name`           | `eth0`             | WAN Interface name (as seen on `ip a` command output  |
| `router_wan_ip_static`          | `false`            | false = DHCP, true is obvious (not implemented yet)   |
| `router_wan_ip_address`         | `192.168.0.1/24`   | WAN IP address (not implemented yet)                  |
| `router_lan_int_name`           | `eth1`             | LAN Interface name (as seen on `ip a` command output) |
| `router_lan_ip_address`         | `192.168.1.1/24`   | LAN IP address (quite self-explanatory, right?)       |
| `router_networkservice_disable` | `true`             | If true, stop and disable network.service             |
| `router_networkmanager_disable` | `true`             | If true, stop and disable NetworkManager.service      |
| `` | `` | |

Dependencies
------------

None. Hopefully.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: router }

License
-------

GPLv3
