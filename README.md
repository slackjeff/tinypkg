# Tinypkg is a low-level package manager, similar to 'dpkg' for Linux distributions, written in Shell POSIX.
With you can: Create, install and remove packages in a universal way!

### Options
-h             : Display help.
-c             : Create package.
-i             : Install package(s).
--fakeroot DIR : Changes installation / from another directory. Used with -i
-r             : Remove package(s).

### USAGE Examples
**Create package**
'NOTE! The package name must be: Software-Versao.tar. If you need to use spaces, replace with _ example: Software_editor-01.0424.tar'
```
tinypkg -c leafpad-0.8.17.tar
```

**Install package**
```
# tinypkg -i /home/slackjeff/bin/leafpad-0.18.17.tar
or
# tinypkg -i leafpad-0.18.17.tar
or Multiples packages
tinypkg -i /tmp/*.tar

```

'Note! If there is more than one package with the same name for example: leafpad-version, leafpad-bin-version. It just shows you and does nothing!'

```
tinypkg -r leafpad
```
**Remove package**

**TODO**:
- Create option to update available packages.
- Make it even faster.
- Remove dirt in the code. (How to replace external tools)
- 
