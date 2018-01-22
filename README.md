# SwiftPlayground.run

[![Platform](https://img.shields.io/badge/Platforms-macOS%20%7C%20Linux-4E4E4E.svg?colorA=28a745)](#installation)
[![Twitter](https://img.shields.io/badge/twitter-@krzyzanowskim-blue.svg?style=flat&colorB=64A5DE&label=Twitter)](http://twitter.com/krzyzanowskim)

Online Swift Playground. Implemented in Swift.

TBA. Checkout http://SwiftPlayground.run

![SwiftPlayground.run](https://swiftplayground.run/assets/screenshot.png)

## Installation

```
$ git clone https://github.com/mikekavouras/OnlineSwiftPlayground.git
$ cd swiftplayground
$ npm install
$ swift run -c release
```

## Development

### Xcode

Generate Xcode project

```
$ swift package generate-xcodeproj
```

### React

Web user interface is build with [React](https://reactjs.org/) and [webpack](https://webpack.js.org/).

```
$ npm run build
```

## Docker

[krzyzanowskim/onlineswiftplayground](https://store.docker.com/community/images/krzyzanowskim/onlineswiftplayground)

Download the latest image:

```
$ docker pull krzyzanowskim/onlineswiftplayground
```

or build docker image by yourself:

```
$ git clone https://github.com/krzyzanowskim/OnlineSwiftPlayground.git
$ cd swiftplayground
$ docker build -t krzyzanowskim/onlineswiftplayground .
```

then run container:

```
$ docker run -d -p 8080:8080 --name onlineswiftplayground -t onlineswiftplayground
```

and wait until docker container is up (usually several seconds).

Playground is available at [http://localhost:8080](http://localhost:8080).
If the docker setup uses VirtualBox, the you can get the IP address from `docker-machine ip` command.

```
$ open http://$(docker-machine ip):8080
```

## Config

Third party frameworks should be copied to `Frameworks` directory (Frameworks are for **macOS** host only)

See `config/` for GitHub auth. sample config.

## Author

SwiftPlayground.run is owned and maintained by [Marcin Krzyżanowski](http://www.krzyzanowskim.com)

You can follow me on Twitter at [@krzyzanowskim](http://twitter.com/krzyzanowskim) for project updates and releases.

## License

Creative Commons Attribution Non Commercial 4.0. See [LICENSE](LICENSE.txt) file.
