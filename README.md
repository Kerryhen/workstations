#Arch
- Deps

```bash
pacman -S git openssh python
```

- Enable sshd service

```bash
systemctl enable sshd && systemctl start sshd
```

Example

```yaml
ssh_banner_enabled: true    # enable ssh banner on login             [true/false]
ssh_banner_text: Arch Linux # banner text for ssh session            [default:hostname]
git_name: User Name         # same as git config --global user.name
git_email: user@email.com   # same as git config --global user.email
virtual_machine: true       # install and secure qemu-guest-agent    [true/false]
desktop_environment: true   # install desktop environment            [true/false]
```

Executando

```bash
ansible-playbook <workstation>.yml --ask-become-pass --limit <host>
```

> `--ask-become-pass` na primeria execução
