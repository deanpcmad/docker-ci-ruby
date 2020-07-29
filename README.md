# deanpcmad Ruby Image for CI builds

Docker Ruby images used with Drone CI.

These are forked from [Codeminer42/docker-ci-ruby](htttps://github.com/Codeminer42/docker-ci-ruby)
and modified to update bundler and install `libsodium-dev`

## Dependencies

The following dependencies are being installed on all images:

* Node.js v12.16.1 and npm
* PhantomJS v2.1.1
* Qt v5 and Xvbf (only on CRuby images)
* Chrome Webdriver (latest stable)

### Ruby images

- `2.7`, `latest` [Dockerfile](https://github.com/deanpcmad/docker-ci-ruby/blob/master/2.7/Dockerfile)
- `2.6` [Dockerfile](https://github.com/deanpcmad/docker-ci-ruby/blob/master/2.6/Dockerfile)
- `2.5` [Dockerfile](https://github.com/deanpcmad/docker-ci-ruby/blob/master/2.5/Dockerfile)

### To generate a new build

```
docker build . -t ci-ruby:2.7
docker tag ci-ruby:2.7 deanpcmad/ci-ruby:2.7
docker push deanpcmad/ci-ruby:2.7
```
