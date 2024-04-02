# 깃허브에서의 Merge 종류 3가지
1. Merge Commit : 두 브랜치를 새로운 commit을 만들어서 merge함 [merge되는 브랜치의 커밋들이 다 살아있음.]
2. Squash and Merge : 마찬가지로 하나의 commit을 새로 만들어서 merge. [merge되는 브랜치들의 커밋을 하나로 묶어서]
3. Rebase and Merge : 커밋의 base를 재설정해서 merge하는 것. [merge conflict 위협이 큼]

# git log
* 커밋 기록 조회하는 명령어
* commit id, data, author, commit이름을 최신커밋 순으로 볼 수 있음.
* --oneline옵션 쓰면 각 커밋들을 한줄에 요약해서 보여줌

# git status
* Changes to be committed, Changes not staged for commit, Untracked files 3가지 상태에 따라 파일을 분류해줌
* 주로 git add다음에 썼던걸로 기억.

---------------------------------------------------
# 커밋 취소 관련 명령어 3가지

# git commit --amend
* 마지막 commit내용을 수정하여 새로운 commit으로 대체하는 명령어. [commit id가 바뀜]
* git commit --amend -m "커밋 메세지" : vim진입 없이 commit메세지 수정
* git commit --amend --no-edit : 메세지 수정없이 commit 수정

# git reset
* git reset --soft <커밋 id> : 커밋취소 + 변경사항이 staging area로 돌아감.
* git reset --mixed <커밋 id> : 커밋취소 + 변경사항이 working directory로 돌아감.
* git reset --hard <커밋 id> : 커밋취소 + 아예 이전커밋으로 돌아감.
  
## 위 두가지 명령어는 함부로 쓰지 않는게 좋고, commit할때부터 신중하게 하자.
## 아래 git revert 명령어를 쓰는게 좋더라

# git revert
* commit을 제거하는 개념이 아니라, 새로운 commit을 만들어서 되돌리는 개념.
* git revert --no-edit "<commit id>" : vim진입 없이 바로 revert
* git revert --no-commit : 직접 commit하지 않고 revert 내용을 staging area에 올림.
