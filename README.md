# Alpine OpenJDK 8 / Docker

[![Docker Status][docker-shield]][docker-link] [![Docker Pulls][pulls-shield]][pulls-link] [![Layers][layers-shield]][layers-link] [![Version][version-shield]][version-link]

A minimal [Alpine Linux](https://hub.docker.com/r/_/alpine/) based [Docker](https://www.docker.com/) 
image with [OpenJDK 8](http://openjdk.java.net)

## Content &nbsp;/

- Alpine Linux ( **3.6** ) with GNU C (glibc)
- OpenJDK ( **8u131** )

## Use this &nbsp;>

### as base image

exactly as you would with any other docker image inside `Dockerfile`

```Dockerfile
FROM greyfoxit/alpine-openjdk8
```

### as pull from Docker Hub

```sh
$ docker pull greyfoxit/alpine-openjdk8
```

### as local build

```sh
$ git clone https://github.com/greyfoxit/alpine-openjdk8.git && cd alpine-openjdk8
$ docker build --no-cache -t greyfoxit/alpine-openjdk8 .
```

### as running container

```sh
$ docker run --rm -it greyfoxit/alpine-openjdk8
```

## Example

```sh
$ echo -e 'public class Main { public static void main(String[] args) { System.out.println("Hello Docker"); } }' > Main.java
$ docker run --rm -v `pwd`:/mnt -w /mnt greyfoxit/alpine-openjdk8 javac Main.java && java Main
```

## Support

Please [file an issue](https://github.com/greyfoxit/alpine-openjdk8/issues) on Github

## License

Released under the [MIT License](#LICENSE) by Greyfox, Inc.

[docker-shield]: https://img.shields.io/docker/build/greyfoxit/alpine-openjdk8.svg
[docker-link]: https://hub.docker.com/r/greyfoxit/alpine-openjdk8

[pulls-shield]: https://img.shields.io/docker/pulls/greyfoxit/alpine-openjdk8.svg
[pulls-link]: https://hub.docker.com/r/greyfoxit/alpine-openjdk8

[layers-shield]: https://images.microbadger.com/badges/image/greyfoxit/alpine-openjdk8.svg
[layers-link]: https://microbadger.com/images/greyfoxit/alpine-openjdk8

[version-shield]: https://images.microbadger.com/badges/version/greyfoxit/alpine-openjdk8.svg
[version-link]: https://microbadger.com/images/greyfoxit/alpine-openjdk8
