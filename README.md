### A playbook to join Centos7 / RHEL7 with Windows Active Directory

Most of the Organizations users and groups are created and managed on Windows Active Directory.  We can integrate our RHEL 7 and CentOS 7 servers with AD(Active Directory) for authenticate purpose. In other words we can join our CentOS 7 and RHEL 7 Server on Windows Domain so that system admins can login to these Linux servers with AD credentials. While creating UNIX users on AD we can map these users to a specific group so that level of access is controlled centrally from AD.

### To run the playbook
ansible-playbook site.yml -i hosts -u root

### Playbook Roles
- base: to install basic packages, iptables and protect grub
- common: has all global variables and handlers
- ldap: main role of the playbook to install sssd, realmd and dependency packages for joining AD