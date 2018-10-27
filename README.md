# C++ Conan Sample

Conan is C++ Dependency Manager. This project is sample for using Conan.

## Install

Install [Conan](https://docs.conan.io/en/latest/installation.html)

Install dependencies

```
$ mkdir build && cd build

$ conan install ..
```

NOTE: All commands are in `build/` dir

for **Mac** `Poco` doesn't have pre-compiled binaries.

```
$ conan install .. --build Poco
```

NOTE: You'll need to have installed `cmake` for this

By default **Mac** uses `clang` compiler. If you wanna use `gcc` use,

```
$ conan install .. --build Poco -s compiler="gcc"
```

## Build

**WIN**

```
$ cmake .. -G "Visual Studio 14 Win64"
$ cmake --build . --config Release
```

**Linux / Mac\***

```
$ cmake .. -G "Unix Makefiles" -DCMAKE_BUILD_TYPE=Release
$ cmake --build .
```

## Run

```
$ ./bin/timer
```
