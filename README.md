# bazel rust template

## Install bazel


on rel based systems.
```
sudo dnf update
sudo dnf copr enable lihaohong/bazel
sudo dnf update
sudo dnf install bazel
sudo dnf copr disable lihaohong/bazel
```


## Install rust
I use rustup.
https://rustup.rs/

## Install devtools  

on rel based systems.
```
sudo dnf update
sudo dnf group install "Development Tools"
```


## sync crates

This command will need to be run once a clean repository.
```
CARGO_BAZEL_REPIN=1 bazel sync --only=crates --enable_workspace
```

## build and run

Check that it works before changing.
```
bazel build //fun:hello
```
run to see that it starts
```
bazel run //fun:hello

```
http://127.0.0.1:3000/
