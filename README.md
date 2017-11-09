
The SnakeHack 2017 Game Server

* [API documentation](https://stair-ch.github.io/snakehack-server/index.html)
* [Event Information](https://snakehack.stair.ch/)
* [STAIR](https://stair.ch/)

![Example Game Animation](docs/game.gif)

## Running With Docker

* Install [Docker](https://docs.docker.com/engine/installation/)
* `docker run -it -p 4000:4000 stairch/snakehack-server`
* Connect to http://localhost:4000

**Note:** Docker runs on a virtual lan so when you add a snake to the game you cannot use `localhost`, use your internal IP instead.

## Building from source

### Prerequisites

* [Erlang/OTP19](https://www.erlang.org/downloads)
* [Elixir v1.4](http://elixir-lang.org/install.html)
* [NPM](http://blog.npmjs.org/post/85484771375/how-to-install-npm)
* [Sass](http://sass-lang.com/install)

```sh
git clone git@github.com:stair-ch/snakehack-server.git`
cd snakehack-server
./scripts/setup
./scripts/dev-server
```

## Testing

```sh
mix test
```

## Building the docker image locally

* `docker build --rm -t snakehack-server .`
* `docker run -it -p 4000:4000 snakehack-server`
* Connect to http://localhost:4000
