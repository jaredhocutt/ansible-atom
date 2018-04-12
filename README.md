# Atom

Installs Atom and installs the Atom packages specified by the user.

## Requirements

None

## Role Variables

| Variable        | Required | Default  | Description                                                                                                                                                                                                                |
| --------------- | -------- | -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `atom_version`  | :x:      | `latest` | Using `latest` will always download the latest version of Atom. You can select a specific version from [here](https://github.com/atom/atom/releases). The value should match the tag (i.e. Atom 1.25.1 would be `v1.25.1`) |
| `atom_packages` | :x:      | `[]`     | A list of Atom packages to install. Packages can be found [here](https://atom.io/packages).                                                                                                                                |

## Dependencies

None

## Example Playbook

```
- hosts: localhost
  vars:
    atom_version: v1.25.1
    atom_packages:
      - file-icons
      - atom-beautify
  roles:
      - jaredhocutt.atom
```
