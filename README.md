## DOCKERFILE
### 1.RUN
패키지 설치 같은 명령
### 2.CMD
```
CMD [ "executable" ]
```
### 3.COPY
호스트OS에서 컨테이너 안으로 복사
```
COPY <호스트OS 파일 경로> <Docker 컨테이너 안에서의 경로>
```
### 4.ADD
원격 파일 다운로드 또는 압축 해제 등과 같은 기능
```
ADD <다운 받을 URL> <Docker 컨테이너 안에서의 경로>
```
### 5.ENV
Dockerfile 또는 컨테이너 안에서 환경 변수로 사용
```
ENV [key] [value]
```
### 6.AVG
Dockerfile 에서만 사용
```
AVG [key]=[value]
```

### 7.WORKDIR
 명령을 실행하기 위한 디렉토리를 지정
```
WORKDIR <directory>
```
## DOCKER CMD-LINE
<https://docs.docker.com/reference/>

### 1.docker build
```
$ docker build [OPTIONS] PATH | URL | -
```
#### flags

#### 1) Tag an image (-t)

```
$ docker build -t vieux/apache:2.0 .
```

#### 2) Specify a Dockerfile (-f)

```
$ docker build -f Dockerfile.debug .
```
### 2.docker run
```
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
```

#### 1) Assign name and allocate pseudo-TTY (--name, -it)

#### 2) Automatically remove the container when it exits(--rm)

#### 3) Add bind mounts or volumes using the --mount flag(--mount)
```
$ docker run -it --rm --name=example --mount type=bind,source=${PWD},target=/src example/example_build:0.1 bash
```