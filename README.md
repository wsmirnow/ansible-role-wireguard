# Wireguard Ansible Role

![lint](https://github.com/wsmirnow/ansible-role-wireguard/actions/workflows/lint.yml/badge.svg)
![molecule](https://github.com/wsmirnow/ansible-role-wireguard/actions/workflows/molecule.yml/badge.svg)

Wireguard is a modern, fast an secure VPN software solution. With this Ansible role you can setup your own Wireguard server. It is designed for use in a road-warier scenario. All traffic would be passed through the Wireguard VPN tunnel in a secure manner.

## Requirements

This role is designed for Debian based systems. We expect you have a running `ufw` firewall on your server.

## Usage

You can apply this role in your Ansible playbook as usual.

```Ansible
---
- name: Deploy Wireguard server
  become: true
  hosts: all
  roles:
    - wsmirnow.wireguard
```

Client key and configuration can be created with `sudo wg-create-client client-name` (replace `client-name` with a name of a client device). This command will show you the client configuration QR code.

## License

[MIT](LICENSE)

## Author

Waldemar Smirnow
