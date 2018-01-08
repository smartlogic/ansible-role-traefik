# Traefik

Basic traefik configuration

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
    - { role: smartlogic.traefik }
```

## License

MIT

## Author Information

SmartLogic. https://smartlogic.io
