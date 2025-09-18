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

## Dependencies

No dependencies on other roles.

## Example Playbook

Make sure to include "selected_option" in your playbook to select the version of
Maya you want to install. Please see vars/main.yml for the available versions.

Example playbook for installing:

```yaml
---
- name: Install Reprise RLM Server
  hosts: all
  vars:
    selected_option: "2v17.0BL1"  # Set the required version here
  roles:
    - rlm_server  
```

## Adding to requirements.yml

If you need to bring this into another Ansible Project you can add it to the `requirements.yml` file examples below:

```yaml
- name: rlm_server
  src: https://github.com/edkonsistent/ansible-role-rlm-server.git
  version: main
```

## Adding to vars/main.yml

If you have a new version of Maya to add, please add the following section to vars/main.yml
within the maya role folder:

```yaml
versions:
  - 'v17.0BL1'
```

Please replace the version code with the new version (i.e 2024_2), replace the download
link with the correct link to the .tgz file from within our Nexus repository and update
the major and minor version appropriately.

You will need to run the below in your project to clone the role:

```bash
ansible-galaxy install -r requirements.yml
```
