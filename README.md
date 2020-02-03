# libpmt
The polymorphic type library from GNURADIO as a standalone library!

# What...and...Why
## 1. What
This is the polymorphic type library, that is currently also integrated in GNURadio itself.
It is used as a serialization/deserialization tool that is used in the GNURadio mesage passing system.

## 2. Why
At the GNURadio Hackfest 2020 at ESA ESTEC I learned that you need to build/install the whole of GNURadio, if you have a
machine that wants to talk to a GNURadio flowgraph on a different machine, e.g. via thrift. I though that was insane.
So with GNURadio Maintainer blessing I started to rip libpmt out of GNURadio.

## Attribution
LibPMT is basically just the pmt directories of GNURadio, bend in shape to compile and build in a standalone fashion, without any GNURadio dependency. Therfor 95% of the code comes directly from [GNURadio](https://github.com/gnuradio/gnuradio). 
I also have to give a huge shoutout and thanks to [Josh Morman](https://github.com/mormj) for his pybind11 branch of GNURadio (https://github.com/mormj/gnuradio/tree/pybind11). I basically just had to copy his prior work to get libpmt up and running!

# Installation

## Get the source
```sh
git clone https://github.com/SpectreJan/libpmt.git
```

## Build the library
```sh
cd libpmt
mkdir build
cd build
cmake -DCMAKE_INSTALL_PREFIX=/home/user/opt/ -G Ninja ../
ninja
ninja test
ninja install
```
