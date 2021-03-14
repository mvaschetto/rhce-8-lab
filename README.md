# rhce-8-lab
Ansible playbook to prepare an environment for practice rhce8 exam for libvirt

> :warning: **This playbook will install kvm and configure OVS on target machine** 
> :warning: **I develop this playbook to practice with ansible. Support in the future is not guaranteed** any advice or improvment are welcome

The environment is based on the Pearson IT certification book: [Red Hat RHCE 8 (EX294) Cert Guide](https://www.pearsonitcertification.com/store/red-hat-rhce-8-ex294-cert-guide-9780136872535)

# Requirments
-------------
Ansible >= 2.10

# Tested distribution
---------------------

1. Debian buster (10)

# How to use
------------
Adjust the example ansible.cfg and inventory per your environment