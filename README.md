# Traefik

Basic traefik configuration

## Install to requirements.yml

```
- src: git+git@github.com:smartlogic/ansible-role-traefik
  name: traefik
  version: 0.1.0
```

## Requirements

None

## Role Variables

- `traefik_version` - Which version of traefik to download
- `traefik_config` - The file to use for `config.toml`
  - Default: `config.toml`

## Dependencies

None

## Example Configuration

```yaml
traefik_confige "{{ playbook_dir }}/files/traefik-config.toml"
```

## Example Playbook

```yaml
- hosts: servers
  roles:
    - { role: traefik }
```

## License

MIT

## Author Information

SmartLogic. https://smartlogic.io
