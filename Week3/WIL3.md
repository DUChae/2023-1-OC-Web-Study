# Week3

- Branch란?
  - 독립적 작업을 진행하기 위한 개념
  - 여러 작업 동시 작업 진행 가능
  - 만들어진 브랜치는 다른 브랜치와 병합(merge)함으로써 , 작업한 내용을 다시 새로운 하나의 브랜치로 모을 수 있다.
  - Master(main) branch
    - 저장소 처음 만들 시 master (main) 브랜치 만들어짐
    - 이 저장소에 새로운 파일 추가 혹은 변경하여 커밋하는 것은 모두 master(main)라는 이름의 브랜치를 통해 처리할 수 있음
    - Check out하지 않는 이상 모든 작업은 master branch에서 이루어진다.
  - 브랜치 전환
    - 처음 설치 시 master 브랜치로 선택 되어있음
    - 체크아웃(checkout) 명령어 통해 원하는 브랜치 전환
    - Head 는 현재 사용 중인 브랜치의 선두 부분을 나타냄
    - Head 이동 시, 사용하는 브랜치 변경
  - 브랜치 통합
    - Merge와 Rebase를 사용하는 방법이 있음
    - Merge
      - 여러 개의 브랜치를 하나로 모을 수 있다.
      - Fast forward(빨리감기) 병합이라고 부른다.
      - 하지만 브랜치를 분기한 이후 master브랜치에 변경 사항이 적용되는 경우도 있다.
      - 이 경우엔 master 브랜치 내의 변경 내용과 새로운 브랜치 내의 변경 내용을 하나로 통합할 필요 있음
      - 따라서 양쪽의 변경을 가져온 merge commit 을 실행
    - Rebase
      - 새로운 브랜치를 master 브랜치에 rebase하면, 새로운 브랜치의 이력이 master 브랜치 뒤로 이동하게 되어 하나의 줄기로 이어진다.
- 복습
  1. URI: Uniform Resource Idenitifer
     1. URI= URN+URL
  2. URL: Uniform Resource Location
     1. 위치로 찾기
     2. 프로토콜 + DNS주소
  3. URN : Uniform Resource Name
     1. 이름으로 찾기
  4. 홍익대학교 홉페이지에서 HTML , CSS, JS무엇인지 확인
     1. HTML : 자료 ( 뼈대)
     2. CSS:UI(살과 옷)
     3. JavaScript : 제어
  - Git add
    - 다음 변경을 기록할 때까지 변경분을 모아놓기 위해서 사용합니다.
  - Git commit
    - 변경된 사항을 로컬 저장소에 기록 ex) 내 컴퓨터
  - Git push
    - 변경된 사항을 원격 저장소에 기록 ex) github
  - Git fetch
    - 원격 저장소에서 커밋된 코드를 임시 브랜치로 다 내려받습니다.
  - Git pull
    - 원격 서버에서 최신 commit들을 내려받아 현재 로컬 브랜치와 자동 병합
  - Git이 관리하는 파일의 4가지 상태
    1. Untracked
    2. Unmodified
    3. Modified
    4. Staged
  - 영역
  1. 작업 디렉토리 : 파일이 저장되어 있는 로컬 디렉토리
  2. 스테이징 역역 : 변경 사항이 일시적으로 저장되는 곳
  3. 저장소 ( 리포지토리 ) 영역 : 변역 사항이 영구적으로 저장되는 곳
