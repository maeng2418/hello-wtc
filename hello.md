### github 연결, 커밋, 업로드

`git remote add origin [https://github.com/maeng2418/test.git](https://github.com/maeng2418/test.git)`
`git pull origin master`
`git add .`
`git commit -m "Update"`
`git push origin master`

### clone 다운로드

`git clone [https://github.com/maeng2418/test.git](https://github.com/maeng2418/test.git)`

### 원격 저장소가 업데이트 되었으면 로컬에 반영

`git pull`

### 변경 또는 추적되지 않는 파일 추가

`git add -u`

### 최근 커밋 수정

`git commit —amend`

(수정 후)

`git push -f`

### 최근 push 취소

`git reset HEAD^`

(수정 후)

`git add .`

`git commit -m "Write commit messages"`

`git push -f`

### 이전 커밋 수정

`git rebase HEAD~ 거슬러 올라가고 싶은 커밋 수 -i`

`pick`을 `reword`로 수정

(수정 후)

`git push -f`

### 브랜치작업

`git branch 브랜치이름(develop)` : 브랜치생성
`git checkout 브랜치이름` : 브랜치선택
수정작업후... (commit까지)
`git checkout master` : 다시 마스터 브랜치선택
`git merge 브랜치이름` : 병합
`git push` : 푸시(깃헙에 업로드)

개발 끝남.
`git branch -d develop` : 브랜치 삭제

### 합병충돌시

해당파일 열어보면 위쪽은 마스터 아래는 브랜치 코드 다른거 보여줌.

### Gitignore

```
$ git rm -r --cached .

$ git add .

$ git commit -m "git ignore add"

$ git push
```