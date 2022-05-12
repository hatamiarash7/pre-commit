# Pre Commit

My pre-commit hooks. You can use these hooks for easier development.

## Configuration

Run all checks:

```yaml
repos:
    - repo: https://github.com/hatamiarash7/pre-commit
      rev: v1.0.3
      hooks:
          - id: ansible_find_unused_variable
          - id: ansible_find_empty_files
          - id: ansible_find_empty_directories
          - id: ansible_fix_readability
          - id: ansible_find_undefined_handlers
          - id: ansible_find_unquoted_values
```

## Hooks

We have these hooks for now. more items will be added gradually.

### Ansible - Find unused variables

This hook can help you find defined variables ( in `defaults/main.yml` or `vars/main.yml` ) that are not used in the role.

```yaml
repos:
    - repo: https://github.com/hatamiarash7/pre-commit
      rev: v1.0.0
      hooks:
          - id: ansible_find_unused_variable
```

### Ansible - Find empty files

This hook can find empty `defaults/main.yml`, `handlers/main.yml` and `vars/main.yml` files.

```yaml
repos:
    - repo: https://github.com/hatamiarash7/pre-commit
      rev: v1.0.0
      hooks:
          - id: ansible_find_empty_files
```

### Ansible - Find empty directories

This hook can find empty directories.

```yaml
repos:
    - repo: https://github.com/hatamiarash7/pre-commit
      rev: v1.0.0
      hooks:
          - id: ansible_find_empty_directory
```

### Ansible - Fix Readability

This hook can improve readability.

```yaml
repos:
    - repo: https://github.com/hatamiarash7/pre-commit
      rev: v1.0.0
      hooks:
          - id: ansible_fix_readability
```

### Ansible - Find undefined handler

This hook can find undefined handlers.

```yaml
repos:
    - repo: https://github.com/hatamiarash7/pre-commit
      rev: v1.0.0
      hooks:
          - id: ansible_find_undefined_handlers
```

### Ansible - Find unquoted values

This hook can find unquoted values.

```yaml
repos:
    - repo: https://github.com/hatamiarash7/pre-commit
      rev: v1.0.0
      hooks:
          - id: ansible_find_unquoted_values
```

## Known Problems

In some cases, you may need change permissions for cloned repository to run checks. For example you have this error :

```lang-none
Executable `/home/username/.cache/pre-commit/<temp name>/scripts/ansible_find_undefined_handlers.sh` is not executable

Find unquoted values that look like a version............................Failed
- hook id: ansible_find_unquoted_values
- exit code: 1
```

You can fix this problems easily :

```bash
chmod ug+x /home/username/.cache/pre-commit/<temp name>/scripts/*
```

---

## Support

[![Donate with Bitcoin](https://en.cryptobadges.io/badge/micro/bc1qmmh6vt366yzjt3grjxjjqynrrxs3frun8gnxrz)](https://en.cryptobadges.io/donate/bc1qmmh6vt366yzjt3grjxjjqynrrxs3frun8gnxrz) [![Donate with Ethereum](https://en.cryptobadges.io/badge/micro/0x0831bD72Ea8904B38Be9D6185Da2f930d6078094)](https://en.cryptobadges.io/donate/0x0831bD72Ea8904B38Be9D6185Da2f930d6078094)

[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/D1D1WGU9)

<div><a href="https://payping.ir/@hatamiarash7"><img src="https://cdn.payping.ir/statics/Payping-logo/Trust/blue.svg" height="128" width="128"></a></div>

## Contributing

Don't be shy to be a contributor 😉

1. Fork it !
2. Create your feature branch : `git checkout -b my-new-feature`
3. Commit your changes : `git commit -am 'Add some feature'`
4. Push to the branch : `git push origin my-new-feature`
5. Submit a pull request

## Issues

Each project may have many problems. Contributing to the better development of this project by reporting them.
