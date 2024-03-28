# 헷갈리는 개념만 정리해보겠습니다.

### git push origin main
main을 origin branch로 설정하여, 앞으로 main branch로는 git push만 해도, push가 되게끔 하는 명령어
바꾸고 싶으면, git push --set-upstream origin <브랜치이름>

### commit할때 commit message를 적길 바란다. (이런 약속이 있어야, 나중에 팀원들 간 커밋메세지를 읽는데 있어, 가독성이 좋아진다.)
* feat : 새로운 기능을 추가한 경우
* refactor : 기존 코드를 개선한 경우
* fix : 버그를 수정한 경우
* chore : 코드 외의 설정을 바꾼 경우
* docs : 문서화
* test : 테스트 코드

### issue
repo에서 작업계획, 토론 및 추적을 위해 사용한다.

### branch naming
"type/(issue번호)-(간략한설명)"

### merge할때는, 3가지 옵션이 존재한다.
1. Create a commit merge [이게 3-way merge인가?]
2. Squash and merge [여러개의 커밋을 하나의 커밋으로 바꾸어 merge시키는 것. 이걸 주로 쓴다고 한다. 커밋기록 신경안쓰고 merge만 할때?]
3. Rebase and merge [base를 재설정해서 커밋기록을 깔끔하게 정리되나, merge conflict가 자주 발생한다.]


### issue 만들때, 이슈 번호가 생기더라. 이 번호는 브랜치 이름 정할때 사용.
* 참고로깃모지라는 이모티콘을 이용하면 꾸미기 좋다.

### branch 삭제할땐, 다른 branch로 이동 후에 삭제를 해야하더라.
* git checkout -b <브랜치이름> : 브랜치 만들면서 이동하기
* git branch -D <브랜치이름> : 브랜치 삭제


