# helloworld-docker-blue-green

# Load Balancer restart

`nginx.conf`가 변경되어 로드 벨런서를 다시 시작하기 위해서는 host PC의 `./nginx` 경로 에서 아래의 명령어를 실행하세요.

```shell
docker rm -f nginx-load-balancer || true
docker-compose -p load-balancer up -d --build
```
