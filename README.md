# go-http-fileserver #


## Purpose ##

This is a simple, lightweight HTTP fileserver that can be run easily from the command line.  We developed it so that we could easily interact with demo websites and their assets.  This even includes CORS support, so you could access resources from different domain names or ports.

*Warning: this does not have any security settings whatsoever.  Anything within any directory below that specified when this is launched will be available from your machine on whatever network can access it!*


## Build ##

### Pre-requisites
- `go 1.11+`

### Steps
Simply clone the repository outside of `$GOPATH` and build with `go build`

```
git clone https://github.com/arindas/go-http-fileserver.git
cd go-http-fileserver/
go build
```

Now feel free to place the produced binary on your `$PATH`

## Usage ##

```> go-http-fileserver --help``` will print out help information.

Typically, just change to the directory you want served, and:

```> go-http-fileserver``` and it will serve that up on **port 80**.

```> go-http-fileserver -p 8080``` to serve on a different port, such as port 8080.

Then just

```CTRL-C``` to kill the server when you are done.
