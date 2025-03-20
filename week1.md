# Git 1주차 정리

## Git이란 무엇이고 왜 사용해야 할까요?
- 파일 변경 사항을 추적하고 협업을 원활하게 할 수 있는 분산 버전 관리 시스템
- 여러 사람이 동시에 작업할 때 충돌을 방지하고, 변경 이력을 남길 수 있음

## 내 파일은 어떻게 관리될까요?
- Working Directory: 현재 작업 중인 파일이 위치하는 공간
- Staging Area: 커밋할 파일을 임시로 저장하는 공간 (git add로 추가)
- Local Repository: 커밋된 파일이 저장되는 공간 (git commit으로 저장)

## Git은 어떻게 사용할까요?
- `git clone <repo_url>`: 원격 저장소를 복제
- `.gitignore`: 특정 파일을 Git이 추적하지 않도록 설정
- `git add <file>` → `git commit -m "메시지"` → `git push`: 변경 사항 업로드
- `git status`: 현재 Git 상태 확인

## 브랜치(branch)란 무엇일까요?
- 독립적인 작업을 진행할 수 있는 새로운 가지
- `git branch <branch_name>`: 브랜치 생성
- `git switch <branch_name>`: 특정 브랜치로 이동
- `git merge <branch_name>`: 다른 브랜치의 변경 사항을 병합

## 커밋 기록은 어떻게 확인할까요?
- `git log`: 모든 커밋 내역 확인
- `git log --oneline --graph`: 간략한 커밋 히스토리 확인
- `HEAD`: 현재 작업 중인 브랜치의 최신 커밋을 가리킴

## Issue와 PR은 무엇이고 어떻게 사용하나요?
- Issue: 작업해야 할 내용을 기록하고 관리하는 기능
- Pull Request (PR): 변경된 내용을 메인 브랜치에 병합하기 위한 요청
- 코드 리뷰를 거쳐 승인된 후 merge를 통해 반영됨

