# Ansible Role: Gitlab Register Runners

Ansible galaxy role to register gitlab runners

## Requirements

None.

## Role Variables

```yaml
timestamp: "{{ ansible_date_time.epoch }}"

runner_services:
  - project_name: "your-project-name"
    instance_url: "https://gitlab.com/"
    token: "PROJECT_CICD_RUNNER_TOKEN"
    description: "project stage"
    tag: "project-stage"
    executor: "shell"

runner_config:
  concurrent: 2
  check_interval: 5
```

## Dependencies

None.

## Example Playbook (using default package)

    - hosts: servers
      roles:
        - role: MahdadGhasemian.ansible-register-runners

## License

MIT / BSD

## Author Information

This role was created in 2023 by [Mahdad Ghasemian](https://mahdad.me/).