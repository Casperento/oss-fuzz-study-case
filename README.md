# OSS-Fuzz Homework Implementation

This repository implements the code to a study case on how OSS-Fuzz can be used to do fuzz testing.

# Dependencies

To setup this project, one needs to install the following dependencies in her system:

```
$ sudo apt install -y make \
                      docker-ce \
                      docker-ce-cli \
                      containerd.io \
                      docker-buildx-plugin \
                      docker-compose-plugin \
                      ...
```
**Note**: find the relative packages for your Linux distro. The project was implemented and tested in a Debian 12 environment.

**TODO**: include instructions for setting up clang.

# Build

To build this project, execute the following commands:

```
$ make all LIB_FUZZING_ENGINE=/path/to/libFuzzer.a
```

# Run

OSS-Fuzz is integrated with a CI/CD system, so deployment must be scalable. Hence, one needs to **build up a docker image** with the following command:

```
$ docker build -t oss-fuzz-homework .
```

After that, she can interact with the image using docker's cli options:

```
$ docker run -ti oss-fuzz-homework
```
