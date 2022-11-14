# Chapter 1 - Go 시작하기

- multiple 모듈의 경우 뒤 챕터 내용에서 서술됨

- `go mod tidy`를 사용해서, 사용중인 혹은 사용하지 않는 모듈에 대한 관리

- package는 관리중이며 Go 도구들이 다운로드 받을 수 있는 경로로 서술해야함.

# Chapter 2 - 모듈 만들기

- export하기 위한 모듈 생성하기. package명을 `main`을 사용하면 안됨. 그러면 호출 모듈에서 해당 모듈이 프로그램이라고 인식해버림

- export하기 위해선 앞글자를 대문자로 사용해야함. [Exported names](https://go.dev/tour/basics/3) 참고하기

- 타입은 코드대로 정의하면 됨

- `main` 패키지 아니면 실행 안됨. (그러면 main으로 두고 나중에 패키지명 바꾸는 식으로 개발하나..? 테스트 코드 작성 쯤 가면 알듯)

# Chapter 3 - 모듈 호출하기

- 해당 모듈이 publish된 경우는 해당 URL을 사용하면 되지만, 로컬 개발 시에는 publish 되지 않았기 때문에 replace로 대처함. 버저닝은 맞춰주면 됨

# Chater 4 - 에러 핸들링

- 함수의 리턴은 복수 값 가능. 에러 발생 시 호출자는 두 번째 반환 값을 체크하게 됨.

- 해당 함수의 호출자는 코드와 같은 방법으로 반환 값을 참조하면 됨

# Chapter 5 - 랜덤 함수

- 모듈 내의 소문자로 시작하는 함수의 경우, 해당 모듈 스코프 내에서만 접근이 가능

- slice의 사이즈를 생략하여 정의할 경우(`[]string`), 동적으로 변할 수 있음을 알림

- `init` 함수의 경우는 프로그램이 시작할 때, 전역 변수가 초기화 되고 난 후, 자동적으로 실행 됨

# Chapter 6 - 여러 키 대응하기

- map 초기화 방법은 `make(map[key-type]value-type)`

- for loop range는 첫번째 요소는 인덱스, 두 번째는 item 값의 복사값이다. 사용이 필요 없는 경우 underscore로 대체한다.

# Chapter 7 - 테스트

- `_test.go`는 테스트 함수 파일임을 알리는 역할

- 패키지 명은 테스트할 패키지와 동일

# Chapter 8 - 컴파일 및 설치

- `build`는 컴파일을 실행하지만 결과를 설치하지는 않음. `install`은 컴파일 및 설치를 수행함

- `GOBIN` 혹은 `PATH`를 추가하면 해당 바이너리 위치가 아니어도 실행이 가능함

- `export PATH=$PATH:/path/to/your/install/directory` , `go env -W GOBIN=/path/to/your/bin`



