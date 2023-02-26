# Ansible Role: .Net Core SDK/Runtime

Installs the [.Net Core SDK/Runtime](https://www.microsoft.com/net) for Ubuntu/RHEL/CentOS.

## Requirements

This role only runs on Ubuntu, RHEL and its derivatives.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    dotnet_package: "dotnet-sdk-5.0"
    dotnet_debian_repo_gpg_key_url: "https://packages.microsoft.com/keys/microsoft.asc"

Use `dotnet_package` variable described above to install specific version of dotnet SDK or runtime.

## Dependencies

None.

## Example Playbook

    - hosts: servers
      roles:
         - ocha.dotnet-core

## License

MIT / BSD

---
