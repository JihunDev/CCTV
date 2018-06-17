# BBB-mjpg-streamer

## About Project

비글본 블랙을 이용한 Web에서 확인할 수 있는 CCTV



## installing

### Download

```shell
$ opkg update
$ opkg upgrade
$ opkg install python python-modules python-pyserial python-numpy python-setuptools python-misc python-pip git
```

### ffmpeg-dev

- 오픈소스 영상 인코딩 라이브러리

```shell
$ opkg install  ffmpeg-dev 
```

### opencv

- 실시간 이미지 프로세싱에 중점 라이브러리

```shell
$ opkg install opencv
```

### Svn 

- 설치

```shell
$ opkg install svn
```

- svn 서버에서 mjpg-streamer 다운로드후 mjpg-streamer-code 폴더에 저장

```shell
$ svn checkout svn://svn.code.sf.net/p/mjpg-streamer/code/ mjpg-streamer-code
```

- 컴파일

```shell
$ cd mjpg-streamer-code/mjpg-streamer-experimental
$ make 
```



## Getting Start

```shell
$ ./mjpg_streamer -i "./input_uvc.so" -o "./output_http.so -p 8080 -w ./www"
```



## License

MIT