# docker-study

## 도커(Docker)
리눅스 응용 프로그램들을 소프트웨어 컨테이너 안에 배치시키는 일을 자동화하는 오픈 소스 프로젝트이다

### docker hub
필요한 소프트웨어를 찾을수 있다<br/>
이미지를 다운로드 받는 행위 - pull

### image
docker hub에서 다운로드해서 로컬에 가지고 있는 프로그램과 같은 부분<br/>
이미지를 실행하는 행위 - run

### container
이미지를 실행하는 부분, 이미지는 여러개의 컨테이너를 가질수있다

### 도커에 아파치 설치해보기
```
docker pull [OPTIONS] NAME[:TAG|@DIGEST]
docker pull httpd
```
### 컨테이너 실행
```
docker run httpd
docker run --name ws2 httpd
```
### 실행 컨테이너 확인
```
docker ps
```
### 컨테이너 종료
```
docker stop ws2
```
### 생성된 컨테이너 시작
```
docker start ws2
```
### 로그 확인
```
docker logs ws2
```
### 컨테이너 삭제
```
docker rm ws2
```

### 도커를 이용한 웹서버
우선 웹서버(아파치,nginx)가 컨테이너에 설치가 됩니다<br/>
이러한 컨테이너가 설치된 운영체제를 docker host 라고 부르며<br/>
하나의 도커 호스트에너는 여러개의 컨테이너가 만들어질수있습니다<br/>
호스트와 컨테이너는 모두 독립적인 실행환경 이기 때문에 호스트와 컨테이너의 포트를 연결해주어야합니다<br/>
즉 포트포워딩을 해주어야합니다
```
docker run -p 80:80 httpd
//호스트포트 : 컨테이너 포트
docker run --name ws3 -p 8081:80 httpd
```

### 컨테이너 내부 명령어 실행
```
docker run -p 80:80 httpd
//호스트포트 : 컨테이너 포트
docker run --name ws3 -p 8081:80 httpd
```

### 호스트 파일 시스템과 컨테이너 연결하기
```
docker run -p 80:80 httpd
//호스트포트 : 컨테이너 포트
docker run --name ws3 -p 8081:80 httpd
```

