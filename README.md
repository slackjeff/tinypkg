# Tinypkg is a low-level package manager, similar to 'dpkg' for Linux distributions, written in Shell POSIX.
With you can: Create, install and remove packages in a universal way!

### Install

**Use tinypkg only with the root user!**
```
chmod +x tinypkg && cp tinypkg /usr/sbin
```

### Options
-h             : Display help. <br>
-c             : Create package.<br>
-i             : Install package(s).<br>
--fakeroot DIR : Changes installation / from another directory. Used with -i<br>
-r             : Remove package(s).<br>

### USAGE Examples
**Create package**

'NOTE! The package name must be: Software-Versao.tar. If you need to use spaces, replace with _ example: Software_editor-01.0424.tar'
```
# tinypkg -c leafpad-0.8.17.tar
```

**Install package**

```
# tinypkg -i /home/slackjeff/bin/leafpad-0.18.17.tar
or
# tinypkg -i leafpad-0.18.17.tar
or Multiples packages
tinypkg -i /tmp/*.tar

```

**Remove package**

'Note! If there is more than one package with the same name for example: leafpad-version, leafpad-bin-version. It just shows you and does nothing!'

```
# tinypkg -r leafpad
```

## If you want to collaborate with the code:
- Keep the code below 250 lines (*Comments Not included*)
- Use only the standard POSIX Shell
- Do not include unnecessary things!

## TODO (Urgent)
- Create option to update available packages.
- Make it even faster.
- Remove dirt in the code. (How to replace external tools)
- Create a post installation script
