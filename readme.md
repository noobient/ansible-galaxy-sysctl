# bviktor.sysctl

## Synopsys

This role lets you set permanent sysctl values. The changes are applied immediately.

## Parameters

| Name | Required | Example | Description |
|---|---|---|---|
| `file` | yes | `99-wireguard` | Filename without extension to be placed under `/etc/sysctl.d`. |
| `option` | yes | `net.ipv4.ip_forward` | sysctl option. |
| `value` | yes | `1` | sysctl value. |

## Examples

```yml
- include_role:
    name: bviktor.sysctl
  vars:
    file: '99-wireguard'
    option: 'net.ipv4.ip_forward'
    value: '1'
```

## Return Values

N/A

## Support

| Platform | Support | Status |
|---|---|---|
| Linter | ✅ | [![Lint](https://github.com/noobient/ansible-sysctl/actions/workflows/lint.yml/badge.svg)](https://github.com/noobient/ansible-sysctl/actions/workflows/lint.yml) |
| AlmaLinux 8 | ✅ | [![AlmaLinux 8](https://github.com/noobient/ansible-sysctl/actions/workflows/almalinux-8.yml/badge.svg)](https://github.com/noobient/ansible-sysctl/actions/workflows/almalinux-8.yml) |
| AlmaLinux 9 | ✅ | [![AlmaLinux 9](https://github.com/noobient/ansible-sysctl/actions/workflows/almalinux-9.yml/badge.svg)](https://github.com/noobient/ansible-sysctl/actions/workflows/almalinux-9.yml) |
| Fedora 37 | ✅ | [![Fedora 37](https://github.com/noobient/ansible-sysctl/actions/workflows/fedora-37.yml/badge.svg)](https://github.com/noobient/ansible-sysctl/actions/workflows/fedora-37.yml) |
| Ubuntu 18.04 | ✅ | [![Ubuntu 18.04](https://github.com/noobient/ansible-sysctl/actions/workflows/ubuntu-18.04.yml/badge.svg)](https://github.com/noobient/ansible-sysctl/actions/workflows/ubuntu-18.04.yml) |
| Ubuntu 20.04 | ✅ | [![Ubuntu 20.04](https://github.com/noobient/ansible-sysctl/actions/workflows/ubuntu-20.04.yml/badge.svg)](https://github.com/noobient/ansible-sysctl/actions/workflows/ubuntu-20.04.yml) |
| Ubuntu 22.04 | ✅ | [![Ubuntu 22.04](https://github.com/noobient/ansible-sysctl/actions/workflows/ubuntu-22.04.yml/badge.svg)](https://github.com/noobient/ansible-sysctl/actions/workflows/ubuntu-22.04.yml) |
