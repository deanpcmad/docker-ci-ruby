# deanpcmad Ruby Image for CI builds

Docker Ruby images used with Drone CI.

## Dependencies

The following dependencies are being installed on all images:

* Node.js v8.11.1 and npm
* PhantomJS v2.1.1
* Qt v5 and Xvbf (only on CRuby images)
* Chrome Webdriver (latest stable)

### Ruby images

- `2.6`, `latest` [Dockerfile](https://github.com/deanpcmad/docker-ci-ruby/blob/master/2.6/Dockerfile)
- `2.5` [Dockerfile](https://github.com/deanpcmad/docker-ci-ruby/blob/master/2.5/Dockerfile)

### To generate a new build

```
docker build . -t ci-ruby:2.6
docker tag ci-ruby:2.6 deanpcmad/ci-ruby:2.6
docker push deanpcmad/ci-ruby:2.6
```
