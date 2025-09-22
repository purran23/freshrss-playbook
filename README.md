# freshrss-playbook
Ansible playbook for setting up Freshrss

## Prerequisites
- This playbook assumes that you have incus remote configured on the host running this playbook.
    - If you wish to run this playbook with ssh instead edit inventory-ssh.yml and rename it to inventory.yml
- The ansible community collection needs to be installed.
    - To install it run ```ansible-galaxy collection install community.general```
## Running this playbook
1. Open a terminal and go into the freshrss-playbook directory.
2. Check vars/keyfile.yml and edit a root db password and a user db password.
3. Check vars/vars.yml that timezone and other settings looks good.
    - version is taken from [FreshRSS github page](https://github.com/FreshRSS/FreshRSS/tags)
3. Run: ```ansible-playbook main.yml```
4. Go to ```https://FreshRSS host IP-address```

## Sources
 - [FreshRSS github page](https://github.com/FreshRSS/FreshRSS)
 - [ansible LXD plugin docs](https://docs.ansible.com/ansible/latest/collections/community/general/lxd_connection.html)
