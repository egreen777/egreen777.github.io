## Github 명령어
- local folder를 Git에서 사용할 수 있도록 초기화: git init
- remote repository를 local로 생성(복제): git clone <주소>
- local file을 remote repository로 등록하는 순서
- git add * (git add . 도 동일)
  - git commit -m "코멘트" : 작업한 내용을 local repository에 등록
  - git push -u origin main : local repository "origin" 을 remote repository "main"에 등록
    - '-u' 옵션은 --set-upstream 으로 이후 동일한 브랜치를 사용할것을 설정 (이후 git push 만으로 동일한 역할 수행, https://victorydntmd.tistory.com/74)

- remote repository 가져오기(통합)
  - git fetch: remote repository의 내용을 local로 가져오나 merge하지 않음
  - git pull: fetch + merge (overwrite가 아니라 merge)

- staging 
  - git add 명령어는 수정내역을 staging영역으로 옮기는 것임 (https://www.daleseo.com/git-add)
    - 현재 작업 공간 (working space)의 내용을 staging에 추가
      - 이 과정을 하는 이유는 git commit은 staging에 있는 파일에만 적용되기 때문
      - git restore를 통해 working space에서 작업한 내용을 모두 취소 (즉 staging의 내용으로 원복) 할 수 있음
    - git add * / git add . : 현재 폴더 및 서브 폴더의 모든 내용을 staging에 추가
    - git add -A : 모든 변경사항을 (어느 폴더애 있던) staging에 추가
    - git add -p : 추가시 하나씩 물어보면서 확인
- status 확인

  - git status: 
   
## GitHub blog 만들기
- Reference: [Github 블로그 만들기 1](https://supermemi.tistory.com/144), [Github 블로그 만들기 2](https://supermemi.tistory.com/145)
- 나중에 확인
  - https://ahnslab.com/21-how-to-start-github-blog/

## Package 관리
- Homebrew: Linux/MAC에서 사용하는 패키지 관리자 (npm, python등)
- npm: 주로 Node.js 패키지를 관리
