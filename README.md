README
------

## How to start

First, set up Ansible on your system:

`pip install ansible` 

You will also need the `pywinrm` package.

`pip install pywinrm`

Finally, you will need to pull the `win_updates` and `chocolatey` collections from 
Ansible Galaxy.

```
$ ansible-galaxy collection install ansible.windows
$ ansible-galaxy collection install chocolatey.chocolatey
```

Next, pull this repo and configure a file named `ansible-hosts` with either the IP addresses 
or hostnames of the desired targets, along with config secrets. See `ansible-hosts.example` for 
more details.

## Running playbooks

To run a playbook:

```
$ ansible-playbook -i ansible-hosts inventory-target playbook-name.yml
```

## Playbooks on offer

- The bms-general-update.yml playbook is intended for running system updates against all computers in the space.
- The bms-lab-config.yml playbook is intended to help configure a lab target after reimaging.
