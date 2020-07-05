# GitHub **프로젝트 미션**

## Git**? GitHub?**

---

- Git은 소스 코드 버전 관리 및 협업을 위해 가장 많이 사용되는 VCS (Version Control System)이다.
- GitHub은 Git을 호스팅 해 주는 사이트로, '소셜 코딩'을 표방하며 가장 유명하고 널리 사용된다.

## **실습 수행**

---

### **미션1: 저장소 생성 및 커밋하기**

- 펼쳐보기

    ### **첫번째 커밋**

    - 깃헙에서 hello-wtc 저장소 생성, 소유자 외에 팀원에게 편집 권한 부여
    - 로컬에 클론
    - git clone, add, commit, push, pull 명령에 대한 설명이 포함된 `hello.md` 생성
    - hello.md add, commit

    ### **두번째 커밋**

    - `hello.md` 에 "좋은 커밋이란 무엇인가?" 에 대한 내용을 간단히 정리해서 추가
    - add, commit, push
    - 원격 저장소에서 확인

    ---

    1. **GitHub repo 생성.**

        ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c1ef8696-fc2d-4ecf-bbcd-c9f974daf61a/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c1ef8696-fc2d-4ecf-bbcd-c9f974daf61a/Untitled.png)

    2. **Clone 생성.**

        `$ git clone [https://github.com/maeng2418/test.git](https://github.com/maeng2418/test.git)`

    3. **버젼 작성자 설정.**

        `$ git config --global user.name "자신의 닉네임"`

        `$ git config --global user.email "자신의 이메일"`

        버전에 포함될 버전을 만든 사람에 대한 정보를 설정합니다. 이 설정은 ~/.gitconfig 파일에 저장되고 1번만 해주면 됩니다.

    4. **Git commit 에디터 설정**

        `$ git config --global core.editor "vim"`

    5. **Markdown 파일 생성. (clone, add , commit, pull 정리)**

        `$ git clone`

        - 원격(remote) 저장소를 지역(local) 저장소로 복제
        - 별도의 remote 설정없이 clone을 통해서 원격 저장소와 연결된다.

        `$ git add <파일이름>` 

        - 작업공간에서 변경이 발생한 파일을 다음 커밋에 포함되도록 예약하는 것
        - 파일은 스테이지 영역(stage area)에 들어가 있게 된다.

        `$ git rm <파일이름>` 

        - git add 명령어의 반대입니다.

        `$ git commit`

        - 파일 및 폴더의 추가/변경 사항들에 대해 기록을 하는 것

        `$ git push`

        - 웹 상의 원격 저장소로 변경된 파일을 업로드하는 것

        `$ git pull`

        - 다른 사람의 변경사항에 대해서 내 로컬에 적용

    6. **훌륭한 Git 커밋 메시지의 일곱 가지 규칙**
        1. 제목과 본문을 빈 행으로 분리한다
        2. 제목 행을 50자로 제한한다
        3. 제목 행 첫 글자는 대문자로 쓴다
        4. 제목 행 끝에 마침표를 넣지 않는다
        5. 제목 행에 명령문을 사용한다
        6. 본문을 72자 단위로 개행한다
        7. 어떻게 보다는 무엇과 왜를 설명한다

    7. **팀원 추가하기.**

        ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/240861f8-db70-442c-8d76-76b8b15af301/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/240861f8-db70-442c-8d76-76b8b15af301/Untitled.png)

        → Manage access 탭을 이용하여 팀원을 추가한다.

### **미션2: 브랜치 생성 및 커밋하기**

- 펼쳐보기
    - `document` 브랜치 생성 및 체크아웃
    - `branch.md` 를 새로 만들고 branch, checkout, merge 에 대한 설명을 작성한다.
    - add, commit, push
    - master에 document 브랜치를 merge한다.
    - master를 push하고 깃헙에서 확인한다.

    1. **브랜치 생성하기**

        `$ git branch 브랜치이름`

        브랜치 생성하기

        `$ git checkout 브랜치이름`

        브랜치 선택하기

        `$ git checkout -b 브랜치이름`

        브랜치 생성하고 선택하기

    2. **Merge 하기**

        `$ git checkout A(브랜치명)`

        A 브랜치로 변경

        `$ git merge B(브랜치명)`

        A 브랜치로 B 브랜치를 병합할 때 (A ← B)

    3. **브랜치 삭제**

        `$ git branch -d B(브랜치명)`

### **미션3: 풀리퀘 보내기**

- 펼쳐보기
    - `document` 브랜치 체크아웃
    - branch.md에 pull request에 대한 내용 추가 및 커밋 생성
    - 깃헙에서 master 저장소에 풀리퀘를 보낸다.
    - 머지하고 확인한다.

    ⇒ 미션2와 미션4를 활용

    `$ git push --set-upstream origin dev`

    Push Stream을 dev로 바꾸고 원격저장소에 dev 브랜치로 업로드 → 원격 저장소에 dev 브랜치가 생성되고, Pull request 요청 가능.

    **원격저장소 브랜치 삭제**

    `$ git push origin --delete 브랜치명`

### **미션4: 저장소 포크 및 풀리퀘**

- 펼쳐보기
    - 저장소 소유자가 아닌 팀원이 원본 저장소를 포크한다.
    - `test` 브랜치를 만들고 `GitHub flow` 에 대한 내용을 간단 정리해서 추가한다.
    - 원본 저장소의 master 브랜치에 풀리퀘를 보낸다.
    - 머지하고 확인한다.

    1. **Fork 뜨기**

        타겟 프로젝트의 저장소를 자신의 저장소로 Fork 한다.

        ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cec8b2a9-577e-482d-aeec-25dc3eb5b44d/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cec8b2a9-577e-482d-aeec-25dc3eb5b44d/Untitled.png)

        → 오른쪽 위에 있는 Fork버튼 눌러서 내 저장소로 복제한다.

    2. Pull request 보내기
        - 다른 사람이 작업중인 repo에 제안(?)하기.
        - 오픈소스 기여할 때 사용.

        ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/85680262-d02c-4705-896a-b4ff37796916/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/85680262-d02c-4705-896a-b4ff37796916/Untitled.png)

        ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d8c6661c-769b-4beb-89ba-ec926ed95e0c/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d8c6661c-769b-4beb-89ba-ec926ed95e0c/Untitled.png)

        ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/29c224a5-d1b6-4f14-9483-2f271c1da90b/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/29c224a5-d1b6-4f14-9483-2f271c1da90b/Untitled.png)

        ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b9498d7c-48f9-4c9a-813b-68cdc0a7b0e6/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b9498d7c-48f9-4c9a-813b-68cdc0a7b0e6/Untitled.png)

        → merge 시키기
``
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
