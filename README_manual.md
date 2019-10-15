1. build a ruby and lein compile environment.
`docker build . -f Dockerfile-build`
2. run last image with a volume
`docker run -v ./zk-web:/usr/src/app ruby-lein-build`
now, you can get a compiled jar, you can find it at target directory with standalone specified, move to zk-web's root directory and named zk-web.jar
3. build zk-web image
`docker build . -f Dockerfile`
all operation finished.
