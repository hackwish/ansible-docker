# AGENTS.md

## Commands

- Syntax check: `ansible-playbook tests/test.yml -i tests/inventory --syntax-check`
- Run test: `ansible-playbook tests/test.yml -i tests/inventory --check --diff`

## Structure

This is an Ansible role. Standard layout:
- `tasks/` - main tasks (01-dependencies, 02-repo, 03-install, 05-users)
- `handlers/` - service handlers
- `defaults/main.yml` - default variables
- `vars/main.yml` - internal variables
- `templates/` - Jinja2 templates

## Testing

Uses tags: `docker-dependencies`, `docker-repo`, `docker-install`, `docker-users`

Run specific tags: `ansible-playbook tests/test.yml -i tests/inventory --tags docker-install`

## Config

`ansible.cfg` sets `roles_path=../` - place this role in parent directory when including in a playbook.

## CI/CD

Semantic-release on push to master/main (requires conventional commits).
