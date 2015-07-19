btrbk packaging
===============

This is the btrbk packaging repository, **used for creating debian
packages**.

The official btrbk git repository is available here:

- git://dev.tty0.ch/btrbk.git
- https://github.com/digint/btrbk.git



Debian
------

### Setting up the build environment

```
# clone the btrbk-packaging repository
git clone -b debian https://github.com/digint/btrbk-packaging.git

# setup upstream branch
cd btrbk-packaging
git remote add -t master -f btrbk https://github.com/digint/btrbk.git
git branch --track upstream btrbk/master

# configure the export directory for gbp
echo -e '[DEFAULT]\nexport-dir = /tmp/debian-export' > ~/.gbp.conf
```


### Build new release

```
gbp pull
gbp buildpackage
```
