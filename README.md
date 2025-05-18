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

Should you have enabled shared folders, run:
```bash
kali@kali:~$ kali-tweaks
```
then:
> In the Kali Tweaks menu, select Virtualization, then Install additional packages and scripts for VMware. Congratulations, you now have two additional tools in your toolbox!

Then:

```bash
kali@kali:~$ sudo mount-shared-folders
```
[Kali docs](https://www.kali.org/docs/virtualization/install-vmware-guest-tools/#adding-support-for-shared-folders-when-using-ovt)

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

- docker setup

## TODO:
- Burp cert
- semi-auto install firefox extensions [ansible-role-firefox](https://github.com/unrblt/ansible-role-firefox)
- Keybindings (launch terminal and etc)
- git-dumper
- rg
- sublime-text [installation](https://www.sublimetext.com/docs/linux_repositories.html#apt)
- strace
- ltrace
- foremost
- volatility 2 & 3

- more tools...
