Github – 원격저장tool
분산 버전 관리 시스템이란? 버전 - 파일이 수정되고 기록하는 시점 이 “시점”을 관리하는 것 – 하나의 버전을 여러명이 불러와 개별적으로 작업할 수 있음

.gitignore로 처리된 파일들은 변화가 생겨도 추적되지 않고, 원격 레포에도 올라가지 않는다.
(보안 문제, 충돌문제, 서버의 BaseURL의 경우에 사용)


변경 없음(unmodified)
변경됨(modified)
스테이지됨(staged)

변경 사항이 생긴 modified 상태일 때 체크포인트를 만드는 일을 commit이라고 함
staged는 commit을 위한 준비 단계로, modified된 파일 중 “선택적으로 해당 파일을 stage”해서 해당 파일만 커밋할 수 있도록 하는 것


여기서 내 폴더에서 read.me 파일을 수정하고
git init
git status
git add . 모든 파일을 staged 상태로 변경 (하나씩 하고 싶을 땐 READ.me로 적으셈)
git commit -m "Update README" 내 PC의 Git 저장소에서 변경 기록을 확정(버전 생성)하는 단계git push origin main 원격 저장소(GitHub 등) 로 기록이 반영
(다른 브런치로 넣고 싶을 땐 main말고 다르게 main2 이렇게 넣으면 됨)
명령어를 입력하니 커밋됨

touch .gitignore 는 git dash 나 WSL(Windows Subsystem for Linux) 같은 환경에서만 바로 사용할 수 있는 명령어
git dash 깔려있으니 이걸로 잘 열어보거나
아니면 걍 텍스트파일 하나 만든다음에 .gitignore로 이름만 바꿔줘도 됨
(.gitigore 쓰니까 잘 text1 파일이 숨겨져 있음)


“서로에게 영향을 주지 않는 작업을 진행하기 위해 브랜치”를 만듦


1.	브랜치 만드는 법
git branch (브랜치 이름)
2.	Switch
git checkout (브랜치 이름) (커밋하지 않으면 브랜치 이동이 불가능한 경우도 있음)
git switch (브랜치 이름)
3.	브랜치 merge하기
git merge (병합할 브랜치)
(보통 브랜치는 merge 명령어를 사용해 병합하지 않습니다. 여러 사람이 한꺼번에 작업하다 보니 충돌의 위험이 있기 때문인데요!) Pull Request라는 것 사용

PR이 Pull Request의 약자였음 : 
메인 브랜치에게 Pull을 받아줄 것을 요청(Request)하는 것



커밋 기록 확인법
1.	git log로 조회

2.	Head
현재 내가 위치하고 있는 브랜치의 최신 커밋을 포인터로 가리키고 있다고 생각하면 됨
(제일 최근에 내가 만졌던 브런치를 가르키고 있음)
