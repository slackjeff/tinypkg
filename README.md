
# SPKG - Simple Package Manager
## Fork [tinypkg](https://github.com/slackjeff/tinypkg)

A low-level package manager, similar to 'dpkg', 'rpm' and 'pkgtool'. Created for Linux distributions, written in Shell POSIX. With tinypkg you can: create, install, list and remove packages in a universal way!

## Installation

**Use tinypkg only with root!**

```
chmod +x spkg && cp spkg /usr/sbin
```

## Options

- **-h**: Displays help.
- **-c**: Creates a package.
- **-i**: Installs packages.
- **-r**: Removes packages.
- **-l**: Lists installed packages.
- **--fakeroot DIR**: Changes installation / from another directory. Used with -i

## USAGE Examples

### Creating a package

'NOTE! The package name must be named as: &lt;name&gt;-&lt;version&gt;.tar
If spaces are needed use underscores. e.g.: Software_editor-01.0424.tar'

```sh
spkg -c leafpad-0.8.17.tar
```

### Installing packages

```sh
# Using absolute path
spkg -i /home/slackjeff/bin/leafpad-0.18.17.tar

# Using relative path
spkg -i leafpad-0.18.17.tar

# Installing multiple packages
spkg -i /tmp/*.tar
```

### Removing packages

'Note! If there are multiple packages with the same name (e.g.: leafpad-version or leafpad-bin-version). It just shows you and does nothing!'

```sh
spkg -r leafpad
```

## If you are willing to contribute:

Make sure you follow these guidelines:

- Keep the code below 250 lines (*Comments not included*)
- Use only the standard POSIX Shell
- Do not include unnecessary things!

## Roadmap

- [ ] Create option to update available packages.
- [ ] Make it even faster.
- [ ] Remove dirt in the code. (replacing external tools)
- [ ] Create a post installation script
- [x] MD5 hash of each package when creating. And check when installing. (security)
