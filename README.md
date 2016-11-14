# DOCKER NGROK IMAGE

## 根据大神的https://github.com/hteen/docker-ngrok.git 修改而来
大神博客 https://hteen.cn/docker/docker-ngrok.html

## BUILD IMAGE

```linux
git clone  https://github.com/401718154/docker-ngrok.git
cd docker-ngrok
docker build -t hteen/ngrok .
```

## RUN
* you must mount your folder (E.g `/data/ngrok`) to container `/myfiles`
* if it is the first run, it will generate the binaries file and CA in your floder `/data/ngrok`

```linux
docker run -idt --name ngrok-server \
-v /data/ngrok:/myfiles \
-e DOMAIN='wixx.ml' hteen/ngrok /bin/sh /server.sh
```
