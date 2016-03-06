# gamsd/revealjs


This is a sample presentation based on revealjs and using the [gamsd/revealjs](https://hub.docker.com/r/gamsd/revealjs/) docker image. You can read about it on my [blog](http://blog.gamsd.com/revealjs-docker-presentations).


## Usage

To run this presentation from this folder, edit the graphs directory as you like and run:

```
> docker run -v `pwd`:/revealjs/talks -p 8000:8000 -d gamsd/revealjs
```

The sample presentation will be available under:
- http://{your_docker_ip}:8000/talks/graphs

> If you're on Linux, you can probably use `localhost` as `{your_docker_ip}`. If you're on Mac using `docker-machine`, your docker IP is probably `192.168.99.100`. Otherwise, check my blog post on [docker-machine networking, IPs and port forwarding](http://blog.gamsd.com/docker-machine-port-forwarding/).
