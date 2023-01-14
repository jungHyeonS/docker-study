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




