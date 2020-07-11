# docker-linux-tools

## _NOTE: I'm consolidating my dockerfile repos into one [dockerfiles](https://github.com/mapitman/dockerfiles) repository_

I use this on my Windows system to run commands like telnet, netcat, etc.

## Usage

```sh
docker run --rm -it mapitman/busybox { telnet, nc, etc. }
```

I set up some functions in my `.bashrc` to run various tools in the Docker container:

```sh
dig () {
    docker run -it --rm mapitman/linux-tools dig $@
}

host () {
    docker run -it --rm mapitman/linux-tools host $@
}

pwgen () {
    docker run -it --rm  mapitman/linux-tools pwgen "$@"
}

telnet () {
    docker run -it --rm mapitman/linux-tools telnet "$@";
}

nc () {
    docker run -it --rm mapitman/linux-tools nc "$@";
}
```

