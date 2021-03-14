# setup-host
------------

## tasks
--------
Check distribution   TAGS: [always]

ensure the directories exists        TAGS: [setup-host]

Create partition on disk {{ data_disk }}     TAGS: [setup-host]        

mount {{ data_disk }}1 on {{ data_path }}    TAGS: [setup-host]        

Check persistent of the mount point by reboot server TAGS: [setup-host]

check mount point {{ data_path }}    TAGS: [setup-host]

check {{ data_path }} mounted        TAGS: [setup-host]

install packages     TAGS: [setup-host]

add {{ ansible_user }} to libvrit group      TAGS: [setup-host]

## vars
-------

| Name | Default value | Optional | Description |
|:-----|:--------------|:---------|:------------|
| data_path | /var/lib/libvirt/images | No | Define where the disks for qemu are stored |