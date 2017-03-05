# Shakers
🐹 + 🐙 = 😽 [![Circle CI](https://circleci.com/gh/ggtools/shakers.svg?style=svg)](https://circleci.com/gh/ggtools/shakers)

A collection of `go-check` Checkers to ease the use of it.

## About this fork

This fork uses the new URL for [gocheck](https://labix.org/gocheck) which is now `gopkg.in/check.v1`. 

## Building and testing it

You need either [docker](https://github.com/docker/docker), or `go`
and `glide` in order to build and test shakers.

### Using Docker and Makefile

You need to run the ``test-unit`` target. 
```bash
$ make test-unit
docker build -t "shakers-dev:master" .
# […]
docker run --rm -it   "shakers-dev:master" ./script/make.sh test-unit
---> Making bundle: test-unit (in .)
+ go test -cover -coverprofile=cover.out .
ok      github.com/ggtools/shakers   0.015s  coverage: 96.0% of statements

Test success
```

### Using glide

- Get the dependencies with `glide up` (or use `go get` but you have no garantuees over the version of the dependencies)
- Run tests with `go test .`
