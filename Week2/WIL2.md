# Week2

## 목표

- Git의 기본 명령어들을 복습
- 로컬 프로젝트를 만든 다음 리모트 저장소와 연결

## 과제목록

### 필수과제

1. git 의 명령어 add, commit , push 는 각각 어떤 역할을 하는지 정리하고 git pull과 fetch의 차이점을 정리하시오.
   1. add
      1. 다음 변경을 기록할 때까지 변경분을 모아놓기 위해서 사용합니다.
      2. 따라서, git commit 명령어를 통해 명시적으로 기록을 남기기 전까지는 아무리 git add명령어를 많이 실행해도 Git 저장소의 변경 이력에는 어떤 영향도 주지 않습니다.
      3. 작업 위치 폴더에 작업한 파일이 있을 경우 , add를 통해서 staging Area로 옮길 수 있습니다.Staging Area는 commit을 진행하기 전의 임시 저장된 상태 정도로 생각하면 될 것 같습니다.
   2. commit
      1. 변경된 사항을 로컬 저장소에 기록 ex) 내 컴퓨터
   3. push
      1. 변경된 사항을 원격 저장소에 기록 ex) github
      2. 현재 폴더를 그대로 업로드 하는 것이 아니라, 지금까지의 이력/버전(commit)을 push하는 것
      3. Working directory , Staging area의 변경 사항들을 원격저장소로 push 되지 않으니 push 전에 git status, git log를 통해서 확인하는 습관 필요
   4. git fetch
      1. 원격 저장소에서 커밋된 코드를 임시 브랜치로 다 내려받습니다.
      2. 내려받은 후 현재 브랜치와 자동 병합하지 않고 , 그렇기에 working directory에도 변화가 없으므로 merge명령어를 이용해 수동 병합해야함
   5. git pull
      1. 원격 서버에서 최신 commit들을 내려받아 현재 로컬 브랜치와 자동 병합
      2. 혼자 개발하는 프로젝트에서는 pull 만 써도 상관 없지만 협업할 때에는 pull의 자동병합은 문제가 될 떄가 많다.
      3. git pull= fetch + merge

### 선택과제

- create-react-app 커맨드를 사용해 프로젝트를 만든 다음 깃허브 리포지토리와 연결하고 리포지토리 링크를 과제 제출 파일에 포함시키시오
  - [https://github.com/DUChae/2023-1-OC-Web-Study.git](https://github.com/DUChae/2023-1-OC-Web-Study.git)
- 진행 과정 중 배운 점이나 발생한 문제점
  - error: src refspec master does not match any
  - error: failed to push some refs to…
    이유
  - 해당 에러는 깃허브에서 pull 없이 push 할 경우 기존 내용을 삭제하거나 하는 문제가 생길 수 있기 떄문에 에러 메시지 발생시키는 것
    해결
    해당 에러가 발생하면 아래의 순서대로 다시 명령어를 입력.
    새로운 깃 리파지토리를 init하고, 다시 push 하는 방법이다.
    **git init**
    **git add .**
    **git commit -m "message"**
    **git remote add origin "github.com/your-repo.git"**
    **git push -u origin master**
    이후 새로운 내용이 추가되거나 수정되었을 때,
    **git add . (또는 특정 파일이나 폴더)**
    **git commit -m "message"**
    **git push -u origin master**
