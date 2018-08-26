# Ansible Role: SSH Keys

Generates key pairs and manages SSH configuration for Mac OS X development.

## Requirements

- ssh-agent
- ssh-add
- ssh-keygen

## Role Variables

Available variables with example values are listed below, for default values see
[`defaults/main.yml`](defaults/main.yml)):

    ssh_keys_dir: "{{ ansible_env.HOME }}/.ssh"
    ssh_keys_pairs:
      default:
        type: rsa
        bits: 4096
        path: "{{ ssh_keys_dir }}/id_rsa"
        email: "user@example.org"
        password: "The ships hung in the sky in much the same way that bricks don’t."
        github:
          - { label: example, token: example }
        bitbucket:
          - { label: example, password: example, user: example }

## Dependencies

## Example Playbook

    - hosts: localhost
      roles:
         - { role: lwalley.ssh-keys }

## License

BSD
