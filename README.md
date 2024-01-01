# mgmt__steam_deck
ansible role for automating the steam deck

# requirements
# variables
readonly_mode: <disable|enable>
# dependencies
# examples
```
---

- name: usage example
  hosts: target_hosts

  tasks:

    tasks:

    - name: disable steamos filesystem protection
      ansible.builtin.include_role:
        name: mgmt__steam_deck
        tasks_from: steamos_readonly.yml
      vars:
        readonly_mode: disable

    - name: refresh pacman keys
      ansible.builtin.include_role:
        name: mgmt__steam_deck
        tasks_from: arch_repository.yml

    - name: enable steamos filesystem protection
      ansible.builtin.include_role:
        name: mgmt__steam_deck
        tasks_from: steamos_readonly.yml
      vars:
        readonly_mode: enable

...
```
