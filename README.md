# ibraimgm's `dwm`

This is my personal fork/configuration of the [dynamic window manager - dwm](https://dwm.suckless.org).

`dwm` isquite unique among most of the window managers by the fact that it does not have a configuration
file; every configuration must be done directly in the source code (which itself is very lean) and recompiled.
Thus, `dwm` users are encouraged to "fork" their on version to customize however they find best.

If you're interested check out [suckless](https://suckless.org) to learn more. You should also read the
[original README](README) of this project.

Applyed patches: [systray](https://dwm.suckless.org/patches/systray/)

## Usage

Simply compile/install and be happy:

```
make
make install

# somewhere, e. g. .xinitrc:
exec dwm
```

Note that the build process copies the `config.def.h` file to `config.h`. My personal customization is done
directly into `config.def.h`, and is merged with the upstream changes on new releases.

## Updating

Just fetch the upstream code and merge in the changes:

```
# first, add the upstream and fetch the changes
git remote add upstream https://git.suckless.org/dwm
git fetch upstream

# check what was changed, etc. and decide to update (or not!)

# do the merge
git merge --no-commit --no-ff upstream/master

# fix the conflicts
git mergetool

# rebuild, test, etc.
# when you're happy, commit and push the changes
git commit
git push origin master
```

## License

See [LICENSE](LICENSE) for details.