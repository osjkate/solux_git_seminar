`[1차 세미나] 깃 기초`
===

## Git & Github

### Git
소스 코드를 효율적으로 관리하기 위해 만들어진 소스 코드 수정에 따른 버전을 관리해주는 시스템
분산 버전 관리 시스템

### GitHub
Git을 사용하는 프로젝트를 지원하는 웹 호스팅 서비스
Git은 로컬 저장소에서 작동해 다른 개발자와 작업 공유 어려움
→ Github로 웹 상에서 클라우드 서버를 통해 로컬 저장소의 코드를 업로드하고 공유

### Git과 GitHub를 사용하는 이유
1. 파일을 수정할 때마다, 언제 무엇이 바뀌었는지 기록해준다. 
2. 기록을 통해 원하는 시점으로 파일을 되돌릴 수 있다. 
3. 다른 사람과 파일을 공유하고 비교할 수 있다. 
4. 여러 사람이 동시에 같은 파일을 작업, 병합할 수 있다. 

<img width="514" alt="스크린샷 2024-05-01 오후 9 05 16" src="https://github.com/osjkate/solux_git_seminar/assets/98140863/50f489ea-5228-4832-857d-71d06c660776">

### 주요 용어

#### 로컬저장소
내 PC에서 관리하는 git 저장소

#### 원격 저장소
로컬 저장소를 업로드 하는 곳   
ex) GitHub, GitLab 등

#### 브랜치
프로젝트의 특정 부분을 독립적으로 개발하기 위한 공간 (분기점)
두 개 이상의 브랜치를 하나로 병합 가능

#### INDEX (= STAGE)
commit을 통해 변경사항들이 반영되기 전, 해당 이력이 저장되는 공간

## Git Bash를 사용해보기
Mac에서는 터미널에 바로 git 명령어 사용 가능하다. 
1. cd 명령어를 사용해서 로컬 저장소로 쓰고 싶은 디렉토리로 이동한다. 
2. Git 사용자를 등록한다. 
<img width="480" alt="스크린샷 2024-05-01 오후 9 06 37" src="https://github.com/osjkate/solux_git_seminar/assets/98140863/e551b1a6-f562-414e-87ab-2ce07e241ddf">
4. Git 사용자를 확인한다.  
<img width="465" alt="스크린샷 2024-05-01 오후 9 06 47" src="https://github.com/osjkate/solux_git_seminar/assets/98140863/7dc061c4-b6c3-4022-b61b-72e82a5f1f76">
    
## Git 기초 명령어

#### `git init`
초기화 명령어
해당 디렉토리가 로컬 깃 저장소로 등록됨
<img width="501" alt="스크린샷 2024-05-01 오후 9 07 28" src="https://github.com/osjkate/solux_git_seminar/assets/98140863/c6c34d2b-2891-4d42-86ca-e846c11aef79">

#### `git status`
지정된 저장소의 현재 상태를 나타냄 
사라진 파일, 생긴 파일 등 업데이트 된 파일과 상태 변경이 필요한 파일들을 알려줌 
<img width="502" alt="스크린샷 2024-05-01 오후 9 07 58" src="https://github.com/osjkate/solux_git_seminar/assets/98140863/d69ba37d-7d45-4858-8861-22f95f6cbccf">

#### `git add (파일명)`
`git add` 뒤에 스테이지에 올릴 파일 이름을 명시함. 
`git add --all` 또는 `git add .` 을 사용하면 status에 나온 변경사항을 전부 스테이지에 올려줌

#### `git commit -m '커밋 내용'`
로컬 저장소의 최종 단계인 Head에 파일을 등록
현재 커밋 대상이 되어 있는 파일(스테이지에 올라와있는 파일들)을 한 번에 커밋
-m 뒤에 버전 관리를 위한 커밋 메시지를 작성해야 함

#### `git remote add origin`
현재의 로컬 저장소를 깃허브에 있는 특정 레퍼지토리에 연결

#### `git remote -v`
연결이 잘 되었는지 확인하는 명령어,
현재 로컬 저장소와 연결된 저장소 url이 반환됨

#### `git push (원격저장소)(브랜치명)`
로컬 저장소에 있던 파일을 원격 저장소로 보냄

#### `git clone`
원격 저장소에 있는 폴더를 로컬로 가져오는 명령어

#### `git branch (브랜치 이름)`
새로운 브랜치를 생성하는 명령어
만들어진 branch를 확인할 때는 `git branch` 사용
브랜치 이동 시에도 `git brance` 사용 

#### `git log`
commit 로그 확인
git의 커밋 히스토리를 보여주는 명령어
commit 된 시간 순서대로 기록되어 있다. 

#### `git diff`
수정내용 확인
2개 파일/commit 간 차이점을 보여주는 명령어
코드의 변경사항을 추적, 검토하는데 사용

#### `git stash`
아직 마무리하지 않은 작업을 스택에 잠시 저장할 수 있도록 하는 명령어
이를 통해 아직 완료하지 않은 일을 commit하지 않고 나중에 다시 꺼내와 마무리할 수 있다. 

#### `git revert`
commit 내용 되돌리기
특정 commit의 내용을 되돌려서 Head에서 추가된 변경사항을 되돌려준다. 

#### `git reset`
commit 내용 취소하기
Head 위치를 아예 바꿔버려 로컬 저장소의 상태를 commit 이전의 상태로 강제로 변경한다. 

## add, commit, push
![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/002c6ef5-2d6f-44c5-a5c1-a9fbdb4d912b/46ed899b-7579-46f8-b36a-d60261f174f2/Untitled.png)

#### add
```java
git add <file or directory>
git add .
```
작업 위치 폴더에 작업한 파일이 있을 경우 add를 통해서 스테이징 영역으로 옮길 수 있다.
스테이징 영역은 commit을 진행하기 전의 임시 저장된 상태 정도로 생각하면 된다. 

#### commit
```java
git commit -m "commit message"
```
스테이징 영역에 추가된 변경 사항을 저장소에 영구적으로 기록하는 명령어
커밋은 변경 사항에 대한 설명과 함께 이루어지며, 커밋 메시지는 해당 변경 사항을 나타내는 명확하고 간결한 내용을 포함해야 한다. 

#### push
```java
git push <remote_name> <branch_name>
```
로컬 저장소의 커밋 기록을 원격 저장소에 업로드하는 명령어
여러 명의 개발자가 협업하는 경우, 로컬 저장소의 변경 사항을 원격 저장소로 백업하고 다른 개발자들과 공유하기 위해 주로 사용된다. 

## fork 와 clone
둘 다 소스 코드를 가져오는데 사용되지만, 그 목적과 사용 방법이 다르다. 

#### **Fork**
- Fork는 다른 사람의 원격 저장소를 자신의 GitHub 계정으로 복제하는 것
- 주로 오픈 소스 프로젝트에서 다른 개발자의 코드에 기여하기 위해 사용된다.
- Fork를 하면 해당 프로젝트의 복사본이 개인 계정으로 생성되며, 이 복사본을 수정하거나 개선한 후에는 원본 프로젝트에 Pull Request를 보내 변경 사항을 제안할 수 있다.

#### **Clone**
- Clone은 원격 저장소의 내용을 로컬 컴퓨터로 가져오는 것
- Git을 사용하여 작업하려는 경우, 프로젝트의 소스 코드를 로컬 환경에 다운로드하여 작업할 수 있어야 한다. 이때 사용하는 명령어가 clone
- clone 명령어는 git 저장소의 URL을 입력하여 사용하며, 해당 URL의 프로젝트를 복제하여 로컬 컴퓨터에 저장한다.
