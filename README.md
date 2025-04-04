# Kali Configuartion Setup 

To ease the bothersome and repetetive chore of setting up a new system, I will use Ansible.

This is inspired by the good ole IppSec: https://github.com/IppSec/parrot-build

## Setup

```bash
git clone https://github.com/Smavl/kali-setup
cd kali-setup
pipx install --include-deps ansible
ansible-playbook main.yml --ask-become-pass
...
```

## Tasks/roles:

