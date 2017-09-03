# Bootstrapping
## Debian/Ubuntu
`/etc/network/interfaces`
```
auto <interface>
iface <interface> inet static
        address <ip address>
        netmask <netmask>

## Raspian
`/etc/network/interfaces`
```
auto <interface>
allow-hotplug <interface>
iface <interface> inet manual
```

`/etc/dhcpcd.conf`
```
interface <interface>
static ip_address=<ip address>
```
