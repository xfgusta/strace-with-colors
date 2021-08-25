# strace, but with colors

This patch adds colored output to the [strace](https://strace.io/) program. Follow the steps below to apply the patch correctly.

## Applying the patch

Clone the [strace git repository](https://github.com/strace/strace) and go to the directory

```
git clone https://github.com/strace/strace
cd strace
```

Checkout the commit `41b753edccb54e62d615aa6f966500a9121165d9`

```
git checkout 41b753edccb54e62d615aa6f966500a9121165d9
```

Get the patch source from [this repository](https://github.com/xfgusta/strace-with-colors) and apply it

```
curl -O https://raw.githubusercontent.com/xfgusta/strace-with-colors/main/strace-with-colors.patch
git apply strace-with-colors.patch
```

Now you are ready to build strace with colors!

## Installing

Run `./bootstrap` and then `./configure`. To compile and install, run `make install` as root.

The program will be in the `/usr/local/bin` directory. You can uninstall running `make uninstall` as root.

## Screenshot

![](screenshot.png?raw=true)