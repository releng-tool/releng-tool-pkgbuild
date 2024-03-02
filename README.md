# releng-tool pkgbuild

This repository manages a [PKGBUILD][pkgbuild] definition used to prepare
a releng-tool release for an Arch Linux system. The `aur` directory is
synchronized with this project's AUR package:

> Arch User Repository - releng-tool \
> https://aur.archlinux.org/packages/releng-tool/

## Commands

Verify `PKGBUILD` is correct:

```
namcap PKGBUILD
```

Build a package using `makepkg`:

```
makepkg
```

Verify the generated package:

```
namcap <built-package-name>
```

To update `.SRCINFO`, the following command can be used:

```
makepkg --printsrcinfo >.SRCINFO
```

[pkgbuild]: https://wiki.archlinux.org/index.php/PKGBUILD
