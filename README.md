# ansible_laptop
Ansible configuration for linux laptops

1. Install Python and Pip


```bash
$ sudo apt install python3 python3-pip

```

2. Install the latest ansible version


```bash
$ UBUNTU_CODENAME=jammy
$ wget -O- "https://keyserver.ubuntu.com/pks/lookup?fingerprint=on&op=get&search=0x6125E2A8C77F2818FB7BD15B93C4A3FD7BB9C367" | sudo gpg --dearmour -o /usr/share/keyrings/ansible-archive-keyring.gpg
$ echo "deb [signed-by=/usr/share/keyrings/ansible-archive-keyring.gpg] http://ppa.launchpad.net/ansible/ansible/ubuntu $UBUNTU_CODENAME main" | sudo tee /etc/apt/sources.list.d/ansible.list
$ sudo apt update && sudo apt install ansible
```

3. Run ansible-pull

```bash
$ sudo ansible-pull -U https://github.com/lugasaji/ansible_laptop.git --extra-vars "home=<home-directory> user=<local_user> group=<group_local_user>"
```
