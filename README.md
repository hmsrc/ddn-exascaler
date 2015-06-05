# ddn-exascaler
Ansible playbooks to deploy a DDN [EXAScaler](http://www.ddn.com/products/lustre-file-system-exascaler/). 

The DVD from DDN is based off of CentOS-6.5 using their sfa12kx-2.1.1 release. The playbooks work on the assumption that you're using cobbler to manage and pxe boot your systems and running CentOS.

1. Define your MDS and OSS servers as `host_vars` files, importantly the MAC addresses.
2. `$ ansible-playbook -i hosts setup.yml`
3. `$ ansible-playbook -i hosts -t cobbler setup.yml`
5. `$ ansible-playbook -i hosts -t boot setup.yml`
6. `$ ansible-playbook -i hosts -t exascaler setup.yml`
