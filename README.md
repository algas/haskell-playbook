Haskell Ansible Playbook
========================

[Ansible](http://www.ansibleworks.com/) playbook that installs a [GHC](http://www.haskell.org/ghc/) from the binary file and a [cabal](http://www.haskell.org/cabal/) from the source file.
Ansibler user need to have no root privilege.

### Requirements

- Ansible 1.4
- Ubuntu or Debian (only tested on Ubuntu 13.04)

### Configure

Make sure that you customise the following files:

- [`hosts`] - hosts to be installed (localhost as default)
- [`group_vars/all`] - `cp group_vars/all.example group_vars/all`

### Preparing

- SSH into the hosts.

### Usage

`ansible-playbook -i hosts site.yml`

### License

Licensed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0).

Copyright 2013 [Masahiro Yamauchi](mailto:sgt.yamauchi@gmail.com).
