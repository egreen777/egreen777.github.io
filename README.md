## Github 명령어
- git init
- local repository 생성: git clone <주소>
- local file을 remote repository로 등록
   - git add *
   - git commit -m "코멘트" : 작업한 내용을 local repository에 등록
   - git push -u origin main : local repository "origin" 을 remote repository "main"에 등록
      - '-u' 옵션은 --set-upstream 으로 이후 동일한 브랜치를 사용할것을 설정 (이후 git push 만으로 동일한 역할 수행, https://victorydntmd.tistory.com/74)

- remote repository 가져오기
   - git fetch: remote repository의 내용을 local로 가져오나 merge하지 않음
   - git pull: fetch + merge (overwrite가 아니라 merge)
   
## GitHub blog 만들기
- Reference: [Github 블로그 만들기 1](https://supermemi.tistory.com/144), [Github 블로그 만들기 2](https://supermemi.tistory.com/145)
- 나중에 확인
   - https://ahnslab.com/21-how-to-start-github-blog/
