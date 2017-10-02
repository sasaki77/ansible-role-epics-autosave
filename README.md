# Ansible Role: EPICS autosave

Installs EPICS autosave on RHEL/CentOS.

## Requirements

- ansible >= 2.3

## Role Variables
Refer to `defaults/main.yml` in detail.
```
epics_autosave_module:
  name: "autosave"
  type: "soft"
  ver: "5-7-1"
  url: "https://github.com/epics-modules/autosave/archive/R5-7-1.tar.gz"
  unarchived_name: "autosave-R5-7-1"
  configure_release:
      - {name: "EPICS_BASE", path: "{{ epics_base_base_name }}", reg: "^(.*)EPICS_BASE(.*)=(.*)$"}
```

## Dependencies

- [ansible-role-epics-base](https://github.com/sasaki77/ansible-role-epics-base)

## Example Playbook
```
- hosts: epics-base
  roles:
    - role: ansible-role-epics-base
    - role: ansible-role-epics-autosave
```

## License

None.

## Author Information

This role was created by Shinya Sasaki.
