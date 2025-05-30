# Traefik

Basic traefik configuration

## Install to requirements.yml

```
- src: git+git@github.com:smartlogic/ansible-role-traefik
  name: traefik
  version: 2.0.0
```

## Requirements

None

## Role Variables

- `traefik_version` - Which version of traefik to download
  - Default: `3.4.1`
- `traefik_checksum` - The sha256 checksum of the traefik download, based on the `linux_amd64` binary, checksums available at https://github.com/traefik/traefik/releases
- `traefik_config` - The file to use for `config.toml`
  - Default: `config.toml` from the role
- `traefik_config_dir` - The folder Traefik will watch for config files
  - Default: `/opt/traefik/config`
- `traefik_config_files` - Array of other files to place in the config_dir
  - Default: `[]`

## Dependencies

None

## Example Configuration

```yaml
traefik_config: "{{ playbook_dir }}/files/traefik-config.toml"
traefik_config_files:
  - "{{ playbook_dir }}/files/app-config.toml"
  - "{{ playbook_dir }}/files/app-ssl.toml"
```

## Example Playbook

```yaml
- hosts: servers
  roles:
    - { role: traefik, tags: ["web", "traefik"] }
```

## License

MIT

## Author Information

SmartLogic. https://smartlogic.io
