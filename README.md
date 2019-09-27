# docker-webssh
Run webssh in docker

## [docker](http://www.docker.com)
Don't know? I am pretty sure this project is not what you are looking for. Just skip it. 
Honestly, I am also studying it, can not say much but really a cool tool you will like. Don't hesitate to try it!

## [webssh](https://github.com/huashengdun/webssh)
A simple web SSH client. Written in Python.

### Features

* SSH password authentication supported, including empty password.
* SSH public-key authentication supported, including DSA RSA ECDSA Ed25519 keys.
* Encrypted keys supported.
* Two-Factor Authentication(time-based one-time password) supported.
* Fullscreen terminal supported.
* Terminal window resizable.
* Auto detect the ssh server's default encoding.
* Modern browsers including Chrome, Firefox, Safari, Edge, Opera supported.

### Preview

![Login](https://github.com/huashengdun/webssh/raw/master/preview/login.png)
![Terminal](https://github.com/huashengdun/webssh/raw/master/preview/terminal.png)

### How it works
```
+---------+     http     +--------+    ssh    +-----------+
| browser | <==========> | webssh | <=======> | ssh server|
+---------+   websocket  +--------+    ssh    +-----------+
```

### How to use
To start a container from this image:
``` bash
$ docker run -d -p 8080:9999 cleberjsantos/webssh
```
The container will start a web application on 8080 port, so you can visit your own ssh client web application via openning localhost:8080 in your browser.

### Environment Variables

``PORT``, ``ADDRESS`` 

These variables, used in conjunction, set a port and address for run application.
