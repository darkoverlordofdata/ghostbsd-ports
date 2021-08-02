# ghostbsd-ports

My own ports, a work in progress

The freebsd ports instructions are exceedingly non-trivial, and written in dense jargon.
Until I can figure out the syntax, I'm using my own makefile which works in a similar fashion.

## www/ice -> PeppermintOS Ice

```
cd www/ice
make
sudo make install

# uninstall
sudo make remove

# remove local copy
make clean

```

```
diff -u /home/darko/GitHub/ice/usr/bin/ice /home/darko/GitHub/ghostbsd-ports/www/ice/work/usr/bin/ice > /home/darko/GitHub/ghostbsd-ports/www/ice/files/patch-ice
diff -u /home/darko/GitHub/ice/usr/bin/ice-firefox /home/darko/GitHub/ghostbsd-ports/www/ice/work/usr/bin/ice-firefox > /home/darko/GitHub/ghostbsd-ports/www/ice/files/patch-ice-firefox

```

```

## devel/desktop -> GitHub Desktop

work in progress

```
cd devel/desktop
make
sudo make install

# uninstall
sudo make remove

# remove local copy
make clean

```
