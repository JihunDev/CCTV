# BBB-mjpg-streamer

## installing
	$ opkg update
	$ opkg upgrade
	$ opkg install python python-modules python-pyserial python-numpy python-setuptools python-misc python-pip git
	
ffmpeg-dev 인스톨(오픈소스 영상 인코딩 라이브러리)

	$ opkg install  ffmpeg-dev 
	
opencv 인스톨(실시간 이미지 프로세싱에 중점 라이브러리)

	$ opkg install opencv

svn 서버사용 인스톨

	$ opkg install svn

svn 서버에서 mjpg-streamer 다운로드후 mjpg-streamer-code 폴더에 저장

	$ svn checkout svn://svn.code.sf.net/p/mjpg-streamer/code/ mjpg-streamer-code
	$ cd mjpg-streamer-code/mjpg-streamer-experimental

컴파일

	$ make 


실행

	$ ./mjpg_streamer -i "./input_uvc.so" -o "./output_http.so -p 8080 -w ./www"