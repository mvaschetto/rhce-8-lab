# net-config
------------

## tasks
--------
Get existing networks        TAGS: [net-config]

enable ipv4 forwarding       TAGS: [net-config]

check the ipv4 forwarding has been enabled correctly TAGS: [net-config]

as been enable ipv4 forwarding       TAGS: [net-config]

Define external natted bridge {{ ext_netnat.name }}  TAGS: [net-config]

Modify external natted bridge {{ ext_netnat.name }}  TAGS: [net-config]

Set autostart on external device {{ ext_netnat.name }}      TAGS: [net-config]

Start external device {{ ext_netnat.name }}  TAGS: [net-config]

Define external bridge interface     TAGS: [net-config]

Modify external bridge interface     TAGS: [net-config]

Modify Host-only internal network    TAGS: [net-config]

Set autostart on external device     TAGS: [net-config]

Set autostart on internal device     TAGS: [net-config]

Activate external network    TAGS: [net-config]

Activate internal network    TAGS: [net-config]

reboot server        TAGS: [net-config]

Get interfaces infos after reboot    TAGS: [net-config]

Check all networks are setup and active      TAGS: [net-config]

## vars
-------
| Name | Default value | Optional | type | Description |
|:-----|:--------------|:---------|:-----|:------------|
| nat_net | true | No | boolean | Define id the KVM server need to be set up for ipv4 forwarding |
| ext_netnat | See example | No | dict | Define the virt ext network with nat enabled |
| ext_nat | See example | No | dict | Define the virt ext network without nat enabled |
| int_nat | See example | No | dict | Define the virt int network (host-only) |

Example for ext_netnat
```yaml
ext_netnat:
  name: "ext-net"
  address: "192.168.100.1"
  subnet_mask: "255.255.255.0"
  dhcp_start: "192.168.100.100"
  dhcp_end: "192.168.100.254"
```

Example for ext_net
```yaml
ext_net:
  name: "ext-net"
  address: "{{ ext-address | default(None) }}"
  subnet_mask: "{{ ext-subnet_mask | default(None) }}"
```

Example for int_net
```yaml
int_net:
  name: "int-net"
  subnet: "10.10.10.0"
  subnet_mask: "255.255.255.0"
  dhcp_start: "10.10.10.100"
  dhcp_end: "10.10.10.254"
```