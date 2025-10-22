## Github 명령어
- local folder를 Git에서 사용할 수 있도록 초기화: git init
   - 실행된 폴더를 Git에 추가 (local repository를 추가 -> Shell 형태가 Git환경으로 변경됨)
   - 폴더를 Git에서 제거하려면 (즉 init을 취소하려면) .git 폴더를 지우면 됨 (rm -r .git)
   - 그런데 그 폴더에 Git 저장소에 들어가면 안되는 파일이 있다면 (e.g. password) 그 파일들은 .gitignore에 넣으면 repository에서 빠짐 

- remote repository를 local로 생성(복제): git clone <Remote repository 주소>
  - remote repository가 local로 복제되면서 local repository와 연결 됨
  - 복제는 필요없고 remote repository와 연결만 필요할때: git remote add origin <Remote repository 주소>

- local file을 remote repository로 등록하는 순서
   - git add * (git add . 도 동일)
   - git commit -m "코멘트" : 작업한 내용을 local repository에 등록
   - git push -u origin main : local repository "origin" 을 remote repository "main"에 등록
      - '-u' 옵션은 --set-upstream 으로 이후 동일한 브랜치를 사용할것을 설정 (이후 git push 만으로 동일한 역할 수행, https://victorydntmd.tistory.com/74)

- remote repository 가져오기(통합)
  - git fetch: remote repository의 내용을 local로 가져오나 merge하지 않음
  - git pull: fetch + merge (overwrite가 아니라 merge)
 
- remote repository 변경
  - git remote remove origin
  - 이후 git remote add origin <Remote repository 주소> 명령으로 새로운 remote reposity와 연결하면 됨

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
- brew: Linux/MAC에서 사용하는 패키지 관리자 (npm, python등)
   - [맥에서 homebrew사용 기본](https://iboxcomein.com/homebrew/)
   - brew update: brew 자체를 최신으로 변경
   - brew upgrade <프로그램명>: 프로그램을 업드레이드 (fomular, cask)
   - brew search: 설치가능한 프로그램 검색
   - 설치된 패키지: python, wget, vscode
- pip: Python 패키지 관리자
- npm: 주로 Node.js 패키지를 관리
