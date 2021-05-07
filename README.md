heroku-buildpack-poppler
------------------------

## Using

Simply add the buildpack to your Heroku app, e.g.

```
heroku buildpacks:add -a MY-APP https://github.com/amitree/heroku-buildpack-poppler
```

## Updating

To update the debian package, run:

```
docker build --build-arg version=21.05.0 -t amitree/poppler:21.05.0 .
docker run --rm -v `pwd`:/mnt amitree/poppler:21.05.0 cp /poppler/build/poppler_21.05.0-1_amd64.deb /mnt/
```
