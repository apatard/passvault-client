# Stupid ansible vault client for [passwordstore](https://www.passwordstore.org/)

This script is a very basic client for ansible-vault. It takes as vault id the
name of the password in pass and it will output it to stdout, as required by
ansible-vault.


It has also support for caching the password into the linux kernel key management facility,
as long as ``keyctl`` is installed.

It's not perfect but I've been using it for years, so maybe it's time to put it online and share it.

```shell
$ pass list
Password Store
└── vault
$ ansible-vault view --vault-id 'vault@/usr/bin/passvault-client' group_vars/all/vault.yml
```
