# Curl (Client URL)
curl(client url) 명령어는 프로토콜들을 이용해 URL 로 데이터를 전송하여 서버에 데이터를 보내거나 가져올때 사용하기 위한 명령줄 도구 및 라이브러리이다. 쉽게말해 예를들어 자바스크립트 환경에서 REST API(http)를 테스트하고싶다면 보통 ajax, fetch 를 이용해 요청을 보내는 것과 같이, SHELL(커맨드라인 환경)에서 REST API(http) 테스트 하고 싶으면 curl 명령어를 이용하면 된다 라고 이해하면 된다.

## Curl 명령어
```Shell
$ curl [options...] <url>
$ curl --help all 
```

| 명령어                      | 설명                                                              |
|--------------------------|-----------------------------------------------------------------|
| -k, --insecure           | https 프로토콜에서 SSL 인증서에 대한 검증없이 연결                                |
| -i, --head               | HTTP 헤더만 보여주고 컨텐츠는 표시하지 않음                                      |
| -D, --dump-header [file] | HTTP 헤더를 file에 기록 (덤프)                                          |
| -L, --location           | --max-redirs 옵션 뒤에 숫자로 몇 번의 리디렉션까지 따라갈 것인지를 적을 수 있다.<br/>기본 값은 50이다. |