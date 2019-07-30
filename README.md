# dockui-app-demo

> Example App for use with [DockUI](https://github.com/yoosername/dockui) - adds Authentication/authorisation capabilities

## Quick start (Docker)

### Build Local Development Image

```shell
$ git clone https://github.com/yoosername/dockui-app-auth.git
$ cd dockui-app-auth
$ npm install
$ docker build --tag dockui/app-auth --file ./Dockerfile-Dev .
```

### Start the App

```shell
$ docker run -it \
  --env HTTP_PORT=3335 \
  --env HTTP_SCHEME=http \
  --network dockui \
  --label DOCKUI_APP=true \
  --label DOCKUI_DESCRIPTOR=dockui.app.yml \
  -p 3335:3335 \
  -v $(pwd):/app \
  dockui/app-auth
```
