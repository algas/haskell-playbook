Haskell Ansible Playbook
========================

[Ansible](http://www.ansibleworks.com/) playbook that installs a [GHC](http://www.haskell.org/ghc/) from the binary file and a [cabal](http://www.haskell.org/cabal/) from the source file.
Ansibler user need to have no root privilege.

### Requirements

- Python
- Ansible 1.4 and over
- SSH server and client

### OS

- Debian, Ubuntu
- CentOS
- Mac OS X

### Preparing

1. Setup ssh server on destination host.
2. Setup ssh client.
3. Install Python and Ansible.
4. Download this playbook.
git clone git@github.com:algas/haskell-playbook.git

### Configure

Make sure that you customise the following files:

- [`hosts`] - hosts to be installed (localhost as default)
- [`group_vars/all`] - configuration arguments
  - Debian, Ubuntu: `cp group_vars/all.example.debian group_vars/all`
  - CentOS: `cp group_vars/all.example.centos group_vars/all`
  - Mac OS X : `cp group_vars/all.example.macosx group_vars/all`

### Usage

Run command:  
`ansible-playbook -i hosts site.yml`

### Notice

* Remember to add PATH to ghc and cabal.  
Add the following line into your shell profile (.bashrc or .bash_profile)  
```
echo "export PATH=$HOME/ghc/bin:$HOME/.cabal/bin:$PATH" >> ~/.bash_profile
```

### License

Licensed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0).

Copyright (c) 2013- [Masahiro Yamauchi](mailto:sgt.yamauchi@gmail.com).

