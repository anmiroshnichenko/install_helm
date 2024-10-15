# Ansible Role: Install Helm

This role installs the [Helm](https://helm.sh) binary on any supported host.

## Requirements

N/A

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    helm_version: 'v3.16.2'
    helm_platform: linux
    helm_arch: amd64

Controls for the version of Helm to be installed. See [available Helm releases](https://github.com/helm/helm/releases/). You can upgrade or downgrade versions by changing the `helm_version`.

    helm_repo_path: "https://get.helm.sh"

The path to the main Helm repo. Unlessy you need to override this for special reasons (e.g. running on servers without public Internet access), you should leave it as the default.

    helm_bin_path: /usr/local/bin/helm

The location where the Helm binary will be installed.

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - role: install_helm

## License

MIT 

## Author Information

This role was created in 2024 by a system administrator at AVM Technology 