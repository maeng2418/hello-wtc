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

### 좋은 커밋이란 무엇인가?
좋은 git 커밋 메시지를 작성하기 위한 7가지 약속
이하 약속은 커밋 메시지를 English로 작성하는 경우에 최적화되어 있습니다. 한글 커밋 메시지를 작성하는 경우에는 더 유연하게 적용하셔도 좋을 것 같네요.

1. 제목과 본문을 한 줄 띄워 분리하기
2. 제목은 영문 기준 50자 이내로
3. 제목 첫글자를 대문자로
4. 제목 끝에 . 금지
5. 제목은 명령조로
6. 본문은 영문 기준 72자마다 줄 바꾸기
7. 본문은 어떻게보다 무엇을, 왜에 맞춰 작성하기

### Branch 작성
git checkout -b branch_names

### Pull Request


### Github flow
Git-flow를 사용했을 때 작업을 어떻게 하는지 살펴보기 전에 먼저 Git-flow에 대해서 간단히 살펴보겠습니다. 
Git-flow에는 5가지 종류의 브랜치로 나누어지게 됩니다.

항상 유지되는 메인 브랜치들(master, develop)과

일정 기간 동안만 유지되는 보조 브랜치들(feature, release, hotfix)이 있습니다. 

- master : 제품으로 출시될 수 있는 브랜치
- develop : 다음 출시 버전을 개발하는 브랜치
- feature : 기능을 개발하는 브랜치
- release : 이번 출시 버전을 준비하는 브랜치
- hotfix : 출시 버전에서 발생한 버그를 수정 하는 브랜치
