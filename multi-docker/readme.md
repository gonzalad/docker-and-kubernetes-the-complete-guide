# Multimodule docker project

## Build

### Build and run all at once

```
docker-compose up
```
OR if you want to force a rebuild of the images:
```
docker-compose up --build
```


### OR build each docker image separately

```
cd client
docker build -f Dockerfile.dev .
cd ..
cd server
docker build -f Dockerfile.dev .
cd ..
cd worker
docker build -f Dockerfile.dev .
```

### Using application

On windows with docker toolbox:
http://192.168.99.100:3050/

Enter a value, a request will be processed asynchronously.
you an view the result by refreshing your browser.

## DEV Build

a docker-compose-dev.yml has been created for DEV purposes (hot-reload)

Not finished, I have the following issues:

* docker-compose volume cannot access local files.
  I need to find a solution (most easy solution is copy/paste local files in %USER_PROFILE% dir, but it's awkward).
