# Ansible Role - NZBHydra

Configure an [NZBHydra](https://github.com/theotherp/nzbhydra) installation.

## Requirements

This role is appropriate for systems using
[systemd](https://www.freedesktop.org/wiki/Software/systemd/) as a service
manager.  The role will abort if it detects that `ansible_service_mgr` is
a defined value other than `"systemd"`.

_This role does not install Couchpotato itself or any of its dependencies_.
You must install Couchpotato prior to applying the role.

## Role Variables

- `nzbhydra_systemd_supplementary_groups`:  a list of groups keyed to the
  NZBHydra systemd unit's `SupplementaryGroups`.  Default is `['downloads']`.
- `nzbhydra_data_dir`: the directory where NZBHydra should store its assets,
  such as its database, PID file, and log files.  Defaults to
  `/var/data/nzbhydra`.
- `nzbhydra_config_file`: the path to NZBHydra's configuration file.  Defaults
  to `{{ nzbhydra_data_dir }}/settings.cfg`.

## Dependencies

None.

## Example Playbook

```yaml
```

## License

MIT

## Author Information

Matt Schreiber <schreibah@gmail.com>
