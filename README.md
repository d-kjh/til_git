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
    git branch -D test
    git branch -v
```

5. branch 합치기

- `주의사항 : main branch에서 test branch를 합쳐야함`

```bash
    git merge 합쳐주고자하는 branch명
```

##### 4-8. git branch 충돌 해결해보기

- github 협업해서 상세히 알아보자

# GitHub

### 1. github 회원가입하기

- https://github.com/

### 2. github 프로젝트(Repository) 생성하기

- 만약 til_git 프로젝트 생성했다면 github에도 생성하자
- public으로 셋팅 : 외부로 소스 공개
- description 은 작성하길 권장 : 프로젝트 설명

### 3. github 인증하기

##### 3-1. 반드시 github에 로그인 된 상태로 시도

##### 3-2. `window키 > 자극 증명 관리자 검색 > Windows 자격 증명`에서 github확인

- 새로 생성하길 권장
- pc 정리 또는 자리 이동시 반드시 삭제

### 4. github 프로젝트 연결하기

##### 4-1. 원격 저장소 주소 지정하기

- `remote`는 원격(인터넷)을 의미
- `add`는 추가를 의미
- `origin`
  - http주소를 간략하게 별칭을 준 의미
  - 단어는 마음대로 가능
  - `원격 이름`을 말함

```bash
    git remote add origin https://github.com/아이디/til_git.git
```

##### 4-2. 원격 저장소 목록 보기

```bash
    git remote -v
```

##### 4-3. 원격 저장소에 소스 등록하기

- 습관적으로 하면 좋은작업
  (Ctrl + s)

```bash
    git add .
    git commit -m "[docs]:최초등록"
```

- 소스 업로드를 `push`라고 함

```bash
    git push -u origin main
```

- `-u`옵션을 붙였으면 이후로는 `git push`만 하면 됨

##### 4-4. 원격 저장소 관리하기

- 목록보기

```bash
    git remote -v
```

- 삭제하기

```bash
    git remote remove 원격이름
```

- 추가하기

```bash
    git remote add 원격이름 https://github.com/아이디/til_git.git
```

- 이름바꾸기

```bash
    git remote rename 현재원격이름 새로운이름
```

##### 4-5. 추천 작업순서

```bash
    git add .
    git commit -m "[docs]:깃학습"
    git push origin main
```

### 5. github의 소스를 다운로드 받아서 작업하는 방법

- github 주소를 주의
- 기준은 `https`로 진행 중
- 코드 소스 기준이 `ssh`면 인증을 다시 처리하는 과정이 필요

##### 5-1. 실습

- 본인PC없이 하고있던 내용을 받고싶을 때
- PC에 환경 설정 진행 (VSCode, git)
- /stdent/`test` 폴더 생성
- github 사이트에 프로젝트를 'clone' 한다
- github 사이트에 Repository를 'clone' 한다

##### 5-2. clone

```bash
    git clone https://github.com/d-kjh/til_git.git .
```

##### 5-3. clone 이후의 작업

```bash
    git status
```

```bash
    git branch -v
    git branch 브랜치명
    git switch 브랜치명
```

`작업`

```bash
    git add .
    git commit -m "작업내용"
```

```bash
    git push origin 브랜치명
```

##### 5-4. git push 이후 작업

- jeju 폴더는 clone을 하여 진행
- til_git 폴더는 clone을 할 필요가 있을까?
  -> til_git 폴더는 이미 git 세팅이 되어있어서 clone은 필요x

##### 5-5. 기존 프로젝트에서 github 브랜치 적용하기

- 기존 프로젝트에서는 clone을 하지 않음
- 기존 프로젝트에서는 `fetch 사용`
- 1. fetch는 github에서 모든 브랜치를 가져옴

```bash
    git fetch --all
```

- 2. 브랜치 전체목록보기(local과 github 브랜치 모두)

```bash
    git branch -a
```

- 3. 새롭게 작업한 `github 브랜치`를 `local 브랜치 생성 > 작업` 동시 진행
     -> ex) `git switch --track -c jeju remotes/origin/jeju`

```bash
    git switch --track -c 생성브랜치명 원격브랜치명
```

### 6. github 브랜치 삭제하기

- github 브랜치 모두 내려받기 및 local 및 github 브랜치 목록 모두 보기

```bash
    git fetch --all
    git branch -a
```

- github의 브랜치 삭제하기
  -> ex) `git push origin --delete jeju`

```bash
    git push 저장소이름 --delete 브랜치이름
```

### 7. 가능하면 브랜치는 삭제하지 않기를 권장

### 8. 가능하면 commit의 내용은 수정,삭제하지 않기를 권장
