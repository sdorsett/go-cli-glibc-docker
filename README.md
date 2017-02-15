# appplant/go-cli
Docker image to build go-cli based binaries against glibc-2.12 (or older), glibc-2.14 (or newer) and musl.

The public images can be found [here][repo] on Docker Hub.


## How to use
For cross-compilation against glibc-2.12:

    $ docker pull appplant/go-cli:glibc-2.12

To compile against glibc-2.14:

    $ docker pull appplant/go-cli:glibc-2.14

To compile against musl:

    $ docker pull appplant/go-cli:musl


## Development
Build each docker image:

    $ docker build -f Dockerfile.[glibc-2.12|glibc-2.14|musl] -t appplant/go-cli:[glibc-2.12|glibc-2.14|musl]

Open a shell to see if all works fine:

    $ docker run -ti appplant/go-cli:[glibc-2.12|glibc-2.14|musl] /bin/sh -l


Finally upload the images:

    $ docker push appplant/go-cli:[glibc-2.12|glibc-2.14|musl] 


## License

The code is available as open source under the terms of the [MIT License][license].

Made with :yum: from Leipzig

© 2017 [appPlant GmbH][appplant]

[repo]: https://hub.docker.com/r/appplant/go-cli/
[license]: https://opensource.org/licenses/MIT
[appplant]: www.appplant.de
