# Bootstrapping
## Debian/Ubuntu

### VLANS
* configure temporary dns
```
sudo rm /etc/resolv.conf
echo "nameserver 192.168.0.1" |sudo tee /etc/resolv.conf
```

* install the `vlan`, `resolvconf`, `python`, and `ifupdown` packages

* remove `netplan` package

* configure network interfaces
```
# /etc/network/interfaces
auto <interface>
iface <interface> inet manual

auto <interface>.<vlan_id>
iface <interface>.<vlan_id> inet static
        address <ip address>
        netmask <netmask>
```

