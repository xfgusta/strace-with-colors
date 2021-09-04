# strace, but with colors

This patch adds colored output to the [strace](https://strace.io/) program. Follow the steps below to apply the patch correctly.

## Arch Linux

Arch Linux users may use the AUR [strace-with-colors](https://aur.archlinux.org/packages/strace-with-colors)

```
git clone https://aur.archlinux.org/strace-with-colors.git
cd strace-with-colors
makepkg -si
```

### Applying the patch

Clone the [strace git repository](https://github.com/strace/strace) and go to the directory

```
git clone https://github.com/strace/strace
cd strace
```

Checkout the tag `v5.14` (latest version)

```
git checkout tags/v5.14
```

Get the patch source from [this repository](https://github.com/xfgusta/strace-with-colors) and apply it

```
curl -O https://raw.githubusercontent.com/xfgusta/strace-with-colors/main/strace-with-colors.patch
git apply strace-with-colors.patch
```

Now you are ready to build and install strace with colors!

### Installing

Run `./bootstrap` and then `./configure`. To compile and install, run `make install` as root.

You may need to install `make`, `automake`, `gcc`. You can actually check all the strace installation instructions [here](https://github.com/strace/strace/blob/master/README-configure).

The program will be in the `/usr/local/bin` directory. You can uninstall running `make uninstall` as root.

## Screenshot

![](screenshot.png?raw=true)
