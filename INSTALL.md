At the moment, ibus-cangjie is not included in any operating system, so you'll
have to build it from source.

We will update these instructions as that changes.

## Build from the sources

### Dependencies

To build IBus Cangjie, you will need the following:

* Python >= 3.2
* the Python 3 GObject bindings
* IBus >= 1.4.1 (note that its GObject-Introspection bindings must be enabled)
* pycangjie
* pycanberra: this is **optional**, only needed to play event sounds,
  especially to give feedback to the user on incorrect inputs. IBus Cangjie
  will fail gracefully if pycanberra is not available though, and just won't
  play any sound.

### Install from a release tarball

_**Note:** There are no release tarballs at this point._

From the root folder of the unpacked tarball, do the usual Autotools dance:

```
$ ./configure
$ make
$ sudo make install
```

### Install from Git

First, you need to clone the development repository:

```
$ git clone git://github.com/Cangjians/ibus-cangjie
```

Then, from the root folder of the Git clone, do the usual Autotools dance:

```
$ ./autogen.sh
$ make
$ sudo make install
```
