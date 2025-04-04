# Kali Configuartion Setup 

To ease the bothersome and repetetive chore of setting up a new system, I will use Ansible.

This is inspired by the good ole IppSec: https://github.com/IppSec/parrot-build

## Setup

```bash
git clone https://github.com/Smavl/kali-setup
cd kali-setup
pipx install --include-deps ansible
ansible-playbook main.yml --ask-become-pass -vv
...
```

## Tasks/roles:

- Configure startup script
    - set keyboard layout
    - rebind capslock to escape
- Packages
    - kali-repo.yml: extra kali packages
    - tools.yml: 
        - pwn/reversing: gdb, ghidra, pwndbg
        - scanning/fuzzing: feroxbuster
        - usefull git repos: secLists, linPeas ...
        - and misc. tools


## TODO:
- Burp cert
- semi-auto install firefox extensions [ansible-role-firefox](https://github.com/unrblt/ansible-role-firefox)
- more tools
