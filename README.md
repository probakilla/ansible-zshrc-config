# Default shell

Ansible role to change the default configuration of zsh

## Role Variables

Stored in defaults folder

```
---
# The path where to install/write zshrc file
zshrc_path: /path/to/zshrc
# The path where to install/write alias file
alias_path: /path/to/alias
# [boolean] If true, override the existing file with blank template then file
# it with other variables. If false, will only update file if the config variable have
# changed.
override_zshrc: false
# [boolean] Same as zshrc but with the alias file
override_aliases: false
# The name of the zsh theme to use
zsh_theme: gentoo
# [list] The list of zsh / oh-my-zsh themes to use
plugin_list:
  - plugin1
  - plugin2
# The list of alias to keep in alias file
alias_list:
  - alias1
  - alias2
# Adding custom paths to the PATH variable into the zshrc file
custom_paths:
CUSTOM=/custom/path/to/add
export PATH=$PATH:$CUSTOM
```
You can find other zsh themes [here](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)

## Howto use this role

This role needs to be included in a playbook
You can install it with *Galaxy*

```bash
ansible-galaxy install -r requirements.yml
```

requirements.yml
```
---

- src: probakilla.apt_install
- src: probakilla.zshrc-config
```

# Requirements

- Ansible 2.4+
- Zsh (if you use default configuration)
- oh-my-zsh
