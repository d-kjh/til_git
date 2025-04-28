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

# GitHub

```

```
