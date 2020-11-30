# helloworld-docker-blue-green

안녕하세요 무중단 배포 코드가 구현되어있는 repose입니다.

추가적으로 CI/CD를 위해서는 [해당 내용을 참고해주세요.](https://velog.io/@ruddms936/Docker%EB%A5%BC-%ED%99%9C%EC%9A%A9%ED%95%9C-%EB%B0%B0%ED%8F%AC-%EC%9E%90%EB%8F%99%ED%99%94-1p2858xt)

http(port:80)으로 접속하기 위해서는 로드 밸런서를 활성화 시켜야합니다. 아래의 헤더를 참고해주세요.

# Load Balancer restart

`nginx.conf`가 변경되어 로드 벨런서를 다시 시작하기 위해서는 host PC의 `./nginx` 경로 에서 아래의 명령어를 실행하세요.

```shell
docker rm -f nginx-load-balancer || true
docker-compose -p load-balancer up -d --build
```
