# Ansible Role: Reprise RLM Server

Ansible role for installing Reprise RLM Server (`rlm_server`)

## Requirements

This role has been tested on Ansible 2.16.0+ against the following Distributions:

  - Rocky 8
  - Rocky 9
  - RHEL 8
  - Windows 11
  - Windows 2022
  - Windows 2025


## Example Playbook

Example playbook for installing:

```yaml
---
- name: Install Reprise RLM Server
  hosts: all
  roles:
    - rlm_server  
```

## Adding to requirements.yml

If you need to bring this into another Ansible Project you can add it to the `requirements.yml` file examples below:

```yaml
- name: rlm_server
  src: https://github.com/konsistent-consulting/ansible-role-rlm-server.git
  version: "v17.0BL1"
```

You will need to run the below in your project to clone the role:

```bash
ansible-galaxy install -r requirements.yml
```
