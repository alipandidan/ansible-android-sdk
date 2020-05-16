# Android SDK Ansible Role

The role is intended to install Android SDK command line tools and SDKs on Ubuntu, Windows and macOS machines.

## Usage

It will install the versions defined under `vars/main.yml`. One can directly change the versions and other settings in that file or while loading the role in playbooks as in:

```yaml
  roles:
    - {role: android-sdk, install_dir.linux: '/path/to/dir'}
    - some-other-role
```

SDKs and packages can be defined as a list in the same file:

```yaml
required_packages: 
  - build-tools;29.0.2
  - platform-tools
  - platforms;android-28
```

### Notes

- macOS target is not tested due to lacking access to a macOS machine.
- Consider using `become: yes` in the playbook when needed.
- Deploying to Ansbile Galaxy will be done soon.
