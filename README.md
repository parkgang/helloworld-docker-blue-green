# helloworld-docker-blue-green

# Load Balancer restart

`nginx.conf`가 변경되어 다시 시작하기 위해서는 아래의 명령어를 실행하세요

```shell
docker rm -f nginx-load-balancer || true
docker-compose -p load-balancer up -d --build
```
