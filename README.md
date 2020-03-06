# Default shell

Ansible role to change the default configuration of zsh

## Role Variables

Stored in defaults folder

```
zshrc_path: The path where to install/write zshrc file
alias_path: The path where to install/write alias file
override_zshrc: If true, override the existing file with blank template then fill
  it with other variables. If false, will only update file if the config variable have
  changed.
override_aliases: Same as zshrc but with the alias file
zsh_theme: The name of the zsh theme to use [see other themes](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)
plugin_list: The list of zsh / oh-my-zsh themes to use
alias_list: The list of alias to keep in alias file
custom_paths: Adding custom paths to the PATH variable into the zshrc file
```

## Howto use this role

This role needs to be included in a playbook
You can install it with *Galaxy*

```bash
ansible-galaxy install -r requirements.yml
```

requirements.yml
```
- src: probakilla.apt_install
- src: probakilla.zshrc-config
```

# Requirements

- Ansible 2.4+
- Zsh (if you use default configuration)
- oh-my-zsh
