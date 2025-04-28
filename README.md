# Git

### 1. git 프로그램 설치

- 프로그램 다운로드 : https://git-scm.com/
- 64-bit Git for Windows Setup. (설치)

### 2. git 버전 확인

- window키 + r : `cmd` 입력

```bash
    git --version
```

- 출력창 확인

### 3. VSCode 에 git 설정하기

##### 3-1. 터미널 환경을 git bash 로 설정하기

- 윈도우, 맥, 리눅스의 명령창을 통일하기 위함
- 관리도구 > 설정
- 설정화면 > 설정검색에 `default:Windows` 입력
- `Git Bash` 선택
- VSCode 재실행 권장

##### 3-2. VSCode git 옵션 설정하기

- 터미널 실행 : 단축키 `Ctrl + 백틱`
- git 버전 확인

```bash
    git --version
```

- 기본 branch명을 `main`으로 설정

```bash
    git config --global init.defaultBranch main
```

- 윈도우, 맥, 리눅스 환경에서 Enter 키 처리를 통일

```bash
    git config --global core.autocrlf true
```

- git commit 명령을 VSCode 에서 작성하도록 설정

```bash
    git config --global core.editor "code --wait"
```

- git 사용자 아이디 설정

```bash
    git config --global user.name "ID"
```

- git 사용자 아이디 설정 확인

```bash
    git config --global user.name
```

- git 사용자 이메일 설정하기

```bash
    git config --global user.email "Email"
```

- git 사용자 이메일 설정 확인

```bash
    git config --global user.email
```

### 4. git 작업하기(실습)

##### 4-1. git 프로젝트 관리 초기화 하기

- 실습

```bash
    git init
```

##### 4-2. git 현재 상태 파악하기

```bash
    git status
```

##### 4-3. git 현재 수정된 내용(파일, 폴더 등) 저장하기

- 원하는 파일만 저장하기

```bash
    git add README.md
```

- 모든 파일 및 폴더 저장하기(권장)

```bash
    git add .
```

##### 4-4. 메모 남기기

- 한 줄 작업 메모

```bash
    git commit -m "git 작업 관련 설명글작성"
```

- 여려 줄 메모 (제목, 상세내용)

```bash
    git commit
```

##### 4-5. commit 내용 컨벤션 알아보기

```bash
[commit타입] : commit 메세지(옵션)
```

- commit 타입 : 작업의 분류
- 옵션 : 이슈 또는 수정이 된 작업커밋 번호 또는 추가정보
- commit 메세지 : 작업내용

1. commit 타입

- `[feat]` : 새로운 기능 추가
- `[fix]` : 버그 수정
- `[docs]` : 문서 수정(README.md)
- `[style]` : 코드의 스타일 변경(띄워쓰기, 세미콜론 등)
- `[refector]` : 코드 리팩토링(기능 변경말고, 코드 정리 등)
- `[test]` : 테스트 코드 추가
- `[chore]` : 기타(빌드 설정, 패키지 업데이트 등)

2. 옵션

- ex) `회원가입 로그인 기능 추가`(새로운 기능 추가)
  이슈 #23번을 해결하고 회원가입 로그인 기능을 추가 했다는 것

```
[feat] : 회원가입 로그인 기능 추가(#23)
```

3. commit 내용

- Enter 키를 기준으로 제목과 내용을 구분한다

```
[docs] : commit 제목

commit 상세 내용 작성
```

##### 4-6. commit 내용 확인하기

- 기존의 commit된 내용을 확인하기
- 상세하게 보기

```bash
    git log
```

- 간략하게 보기

```bash
    git log --oneline
```

- 하나의 commit 상세하게 보기

```bash
    git show commitID
```

1. 각 항목 관련 사항 이해하기

- commit : 고유한 commit 번호(id)
- Author : 작성자
- Date : 날짜
- massege : 상세 내용

##### 4-7. branch 작업해보기

- `나뭇가지`라는 의미로 원 줄기로부터 파생되는 것을 말함
- 원 `소스`로부터 파생한 새롭게 `분기한 소스`관리를 말함
- branch 생성시에는 add와 commit이 완료되어야 함

1. branch 생성하기

```bash
    git add .
    git commit -m "[docs]:branch test"
    git branch test
```

2. branch 목록보기

```bash
    git branch -v
```

3. branch 이동하기

```bash
    git switch test
```

4. branch 삭제하기

```bash

```

5. branch 합치기

```bash

```

# GitHub

```

```
