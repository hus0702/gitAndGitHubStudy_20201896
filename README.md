
GitHub UPL : <https://github.com/hus0702/gitAndGitHubStudy_20201896>

# 과제2 보고서 - git & GitHub 학습하기

20201896 황유석

<br><br>

--- 

# $ git config

막 git을 다운받았다면, 본격적으로 git을 사용하기 전에 사용 환경을 적절히 설정해 주어야 합니다.

따라서 git에 사용자 정보에 대한 정보를 제공하고자 합니다.

이를 위해 다음 git 명령어를 사용하겠습니다.

>     $ git config --global user.name "hus0702"
>   
>     $ git config --global user.email hus0702@naver.com
>   
>   ![config](https://user-images.githubusercontent.com/81548468/117530465-48ae0580-b018-11eb-82d8-537cfd5af634.jpg)

또한, 다음 git 명령어를 사용하여 사용자가 설정한 모든 것을 바로 확인할 수 있습니다.

>     $ git config --list
>   
>   ![list](https://user-images.githubusercontent.com/81548468/117530478-55caf480-b018-11eb-95f3-d31798d16d08.jpg)
<br><br><br>

---

# $ git init

현재 문서는 아무것도 작성되지 않은 상태이며, git의 도움도 받지 못 하는 상태입니다.

이제 이 문서의 버전관리를 위해, git이 문서를 관리할 수 있도록 만들어주고자 합니다.

이를 위해 다음 git 명령어를 사용하겠습니다.

>     $ git init
> 
> ![init](https://user-images.githubusercontent.com/81548468/117530477-5499c780-b018-11eb-9492-a00213aa4032.jpg)

다음 명령어를 통해 .git 이라는 하위 디렉토리를 만들 수 있으며, 이 .git 디렉토리는 저장소에 필요한 뼈대 파일이 들어 있습니다.

<br><br><br>

---

# $ git add / $ git commit / $ git status

.git 디렉토리가 생성되었다면, 이제 본격적으로 버전 관리를 하기 위해 현재 진행 상황을 저장하고 git이 이를 관리하도록 하고자 합니다.

이에 따라, 우선 파일을 새로 추적하게 해준 후 커밋 과정을 거칠 필요가 있습니다.

파일을 새로 추적하게 해주는 콘솔 명령은 다음과 같습니다.

>     $ git add Markdown_Tutorial.md
>
> ![add](https://user-images.githubusercontent.com/81548468/117530451-3cc24380-b018-11eb-9bf8-a1f2ccaa2a67.jpg)

add 명령어를 통해 git은 특정 파일을 추적할 수 있으며, 동시에 이 파일이 곧 커밋에 추가될 상태라는 것을 나타낼 수 있습니다.

또한, 커밋을 하는 콘솔 명령은 다음과 같습니다.

>     $ git commit 

혹은, 다음과 같은 구문으로 인라인으로 메시지를 첨부할 수도 있습니다.

>     $ git commit -m "initial project version"
>
> ![commit](https://user-images.githubusercontent.com/81548468/117530460-46e44200-b018-11eb-8c9d-038161ab7657.jpg)

commit 명령어를 통해 git은 add 명령어를 통해 추적하고 있던 진행 상황을 저장하고 관리할 수 있게 됩니다.


위의 사진에서 나와있듯이, 각각의 단계에서 파일의 상태를 확인하려면 다음 콘솔 명령을 사용하면 됩니다.

>     $ git status

status 명령어를 활용하면 지금 작업하고 있는 파일을 커밋하였는지 등에 대해 간단하게 알아볼 수 있습니다.

<br><br><br>

---

# GitHub에 문서 업로드하기 / $ git remote

이제는 이 파일을 GitHub에 업로드하고 GitHub를 통해서도 버전을 관리하고자 합니다.

GitHub를 통해 레파지토리를 생성하면 다음과 같은 코드를 찾을 수 있습니다.

![GH command](https://user-images.githubusercontent.com/81548468/117530476-52d00400-b018-11eb-98ce-d3db521b1a3d.jpg)

해당 코드를 콘솔에 그대로 입력합니다.

![GH command 2](https://user-images.githubusercontent.com/81548468/117530472-4e0b5000-b018-11eb-90b6-26c201f4698b.jpg)

그러면 다음과 같이 GitHub에 파일이 올라갔다는 알림을 확인할 수 있습니다.

<br><br>

만약 한 파일에 대해 위와 같은 방법으로 업로드하게 된 GitHub 의 원격 레파지토리의 개수를 구하고 싶은 상황이 온다면 다음 콘솔 명령어를 사용하면 됩니다.

>     $ git remote
>
> ![remote](https://user-images.githubusercontent.com/81548468/117530490-654a3d80-b018-11eb-9cdd-0e3466774213.jpg)

이처럼 remote 구문을 활용하면 어떤 파일에 등록되어 있는 리모트 저장소의 개수를 쉽게 파악할 수 있습니다.

<br><br><br>

---

# $ git push / $ git clone / $ git pull

현재 문서는 Markdown 구문을 적기 위한 틀을 완성하였고, 지금까지 작성한 이 파일을 GitHub에 업로드하고자 합니다.

이 경우, 다음 콘솔 명령어를 사용하면 됩니다.

>     $ git push origin main
>
> ![push](https://user-images.githubusercontent.com/81548468/117530487-5fecf300-b018-11eb-8072-05bb8989edab.jpg)

push 명령어를 활용하면 원격 레파지토리인 origin에 main에서 이루어진 변경점을 origin 파일에도 적용할 수 있습니다.

<br><br>

이 작업 이후, 외부에서 다른 컴퓨터로 접속하여 GitHub에 업로드해두었던 문서를 계속 작성하고자 합니다.

이 경우, clone 명령어를 콘솔에 입력하면 됩니다.

>     $ git clone https://github.com/hus0702/gitAndGitHubStudy_20201896
>
>![clone](https://user-images.githubusercontent.com/81548468/117530456-4481e800-b018-11eb-9947-dbb369b49e7b.jpg)

clone 명령어를 콘솔에 입력할 경우, 기존에 작업하던 파일이 없는 환경에 접속했을 때 프로젝트 내역을 복사받아 해당 파일에 대한 작업을 할 수 있습니다.

만약 이와 유사하게 기존에 작업하던 파일은 없지만 구버전의 파일은 있을 경우, 다음 콘솔 명령어를 사용하여 작업 변경점만을 다운받을 수도 있습니다.

>     $ git pull origin main
>
>![pull](https://user-images.githubusercontent.com/81548468/117530486-5cf20280-b018-11eb-8ed2-4ff3069deb69.jpg)

<br><br><br>

---

# $ git branch / $ git checkout

현재 문서는 Markdown의 여러 구문들에 대한 설명을 markdownguide 사이트의 Basic Syntax가 커버하는 순서대로 틀에 맞춰서 작성중인 상태에 있습니다.

이 때, 가독성을 고려하여 문서에 수평선, 강조 표시 등을 다양하게 활용한 버전을 몇 가지 만들어보고자 합니다.

이를 위해 git 명령어 branch를 사용할 수 있습니다.

>     $ git branch layout1
>
>     $ git branch layout2
>
>![branch](https://user-images.githubusercontent.com/81548468/117530453-4055ca80-b018-11eb-8378-2f7b0377861a.jpg)

git 명령어 branch를 활용하면 main 파일에는 변화를 주지 않은 채 서로 다른 두 가지 방식으로 문서를 작성해볼 수 있습니다.

생성한 branch 목록은 다음의 git 명령어를 통해 볼 수 있습니다.

>     $ git branch
>
>![only_branch](https://user-images.githubusercontent.com/81548468/117530484-5b283f00-b018-11eb-95dd-24f69b385401.jpg)

또한, 생성한 branch 중 어느 한 곳으로 이동해서 해당 branch에 대한 문서 작성을 수행하고 싶을 때는 git 명령어 checkout을 이용해야 합니다.

우선 앞서 branch 명령어를 통해 layout1과 layout2의 두 branch를 생성했고, 이제 문서 작성을 위해 layout1 branch로 이동하여 문서를 작성하고자 할 때의 checkout 명령어는 다음과 같습니다.

>     $ git checkout layout1
>
>![checkout](https://user-images.githubusercontent.com/81548468/117530454-421f8e00-b018-11eb-9a41-3da614b4421c.jpg)

이렇게 checkout 명령어를 통해 서로 다른 branch로 이동하고, 각각 add, commit 명령어를 수행하고 변경 사항을 저장함에 따라 서로 다른 버전의 문서를 작성할 수 있습니다.

<br><br><br>

---

# $ git merge / $ git rebase

현재 layout1과 layout2의 작성이 완료된 상황이며, 그 중 layout2 branch의 작업을 main branch에 적용시키려고 합니다.

이 때, 어떤 branch의 변경점을 다른 branch에 적용시키고 싶을 때 사용할 수 있는 콘솔 명령은 다음과 같습니다.

우선, `$ git checkout main` 코드를 통해 변경점을 적용하고자 하는 main branch로 돌아옵니다.

그 후, git 명령어 merge를 사용합니다.

>     $ git merge layout2
>
>![merge](https://user-images.githubusercontent.com/81548468/117530483-595e7b80-b018-11eb-8aaf-4263c1f22dfb.jpg)

git 명령어 merge를 활용하면 손쉽게 다른 branch의 진행 상황을 자신이 원하는 branch에 적용시킬 수 있습니다.

또한, git 명령어 rebase를 통해서도 위와 같은 작업을 수행할 수 있습니다.

>     $ git rebase layout2

Markdown 문서의 7번, 12번, HTML 파트는 작성한 레이아웃이 필요 없겠다고 판단하여, 세 파트를 각각의 branch로 쪼개어 수정한 후 7번과 12번은 merge로, HTML 파트의 수정본은 rebase로 합치겠습니다.

결과는 다음과 같습니다.

![rebase](https://user-images.githubusercontent.com/81548468/117530489-62e7e380-b018-11eb-8d33-b6bde1b123de.jpg)

GitHub 레파지토리에도 나와있듯이 merge 구문과 rebase 구문 둘 다 문제 없이 매끄럽게 합쳐진 것을 알 수 있습니다.

rebase 명령어를 활용하면 merge 명령어를 활용하여 branch를 합쳤을 때와 비교했을 때 히스토리가 더욱 깔끔하다는 특징이 있습니다.

<br><br><br>

---

# $ git log

git log 명령어를 활용하면 지금까지 Markdown 문서를 작성하면서 줬던 변화를 한번에 관찰할 수 있습니다.

git log 명령어의 구문은 다음과 같습니다.

>     $ git log
>
>![log](https://user-images.githubusercontent.com/81548468/117530481-5794b800-b018-11eb-8901-acd55ddc1ebc.jpg)

<br><br><br>

---

# $ git tag

현재 필요한 문서 작업을 끝낸 상태입니다. 보다 효율적이고 직관적인 버전 관리를 위해, 지금 완성한 문서를 v1.0으로 두고 변경점이 있을 때마다 버전 수를 늘려나가고자 합니다.

이 때, 태그를 활용하면 이를 훨씬 수월하게 표기할 수 있습니다.

우선, `$git log` 명령어로 태그를 붙일 시점의 앞자리 6개의 글자를 확인합니다.

이에 대해, 이미 작성된 파일에 대한 git tag 명령어의 구문은 다음과 같습니다.

>     $ git tag -a v1.0 번호

명령어를 입력하면 vi 편집기가 나오는데, i를 누른 후 원하는 정보를 입력하고 ESC > :wq 를 누르면 tag가 생성된다.

이제 git show 명령어를 활용하면 v1.0 태그를 붙인 시점에 대한 정보를 쉽게 얻을 수 있습니다.

git show 명령어의 구문은 다음과 같습니다.

>     $ git show v1.0
>
> ![show](https://user-images.githubusercontent.com/81548468/117530493-67140100-b018-11eb-961b-579968c25c9a.jpg)

<br><br><br>

---

# $ git reset --hard

현재 필요한 문서 작업은 끝냈으며, 추가로 짜잘한 설명글을 작성한 상태입니다.

여기서 추가로 작성한 짜잘한 설명글이 오히려 가독성을 해친다고 판단하여 제거하고자 합니다.

그러나, 코드 중간중간에 설명글에 해당하는 코드를 끼워놔서 일일이 제거하는 것이 힘든 상황입니다.

따라서 필요한 문서 작업만 끝내고 커밋했던 과거 진행 상황으로 돌아가고자 합니다.

이를 위해 git 명령어 reset을 사용할 수 있습니다.

우선 `$ git log` 콘솔 명령을 통해 돌아갈 시점의 일련 번호를 찾아야 합니다.

![제거 - log](https://user-images.githubusercontent.com/81548468/117530495-68ddc480-b018-11eb-8e18-c0afacbacb6b.jpg)

일련번호의 앞자리 6개 리터럴만을 취한 후, 다음 구문에 활용합니다.

>     $ git reset 4d753d --hard
>
> ![제거성공](https://user-images.githubusercontent.com/81548468/117530497-6bd8b500-b018-11eb-8077-790074b099b7.jpg)

다시 `$ git log` 콘솔 명령을 사용하면 돌아온 시점 이후의 변화가 모두 없어졌음을 확인할 수 있습니다.

**단,** 지금 상태에서 만약 push를 통해 GitHub에 지금 작업중인 파일을 업로드하려고 하면 에러가 뜹니다.

이는 원격 저장소 origin의 커밋 히스토리보다 현재 로컬 저장소의 커밋 히스토리가 뒤쳐졌기 때문입니다.

따라서, 다음 콘솔 명령어를 통해 강제로 push 명령을 실행해야 합니다.

>     $ git push -f origin main

![force push](https://user-images.githubusercontent.com/81548468/117530469-4ba8f600-b018-11eb-87d7-23933c299f42.jpg)

--hard 옵션을 붙인 reset 명령어를 활용하면 이처럼 돌아가고 싶은 시점으로 돌아오면서, 해당 시점 이후의 변화는 제거하는 기능이 있다는 것을 알 수 있습니다.

<br><br><br>

---
# 명령어 목록으로 구성된 표

| 명령어  | 사용 여부  | 설명 부분 링크 |
| :---: | :---: | :---: |
| add | ㅇ | [add](#-$-git-add-/-$-git-commit-/-$-git-status) |
| branch | ㅇ | [branch](#-$-git-branch-/-$-git-checkout) |
| checkout | ㅇ | [checkout](#-$-git-branch-/-$-git-checkout) |
| clone | ㅇ | [clone](#-$-git-push-/-$-git-clone-/-$-git-pull) |
| commit | ㅇ |  [commit](#-$-git-add-/-$-git-commit-/-$-git-status) |
| config | ㅇ | [config](#-$-git-config) |
| init | ㅇ | [init](#-$-git-init) |
| log | ㅇ | [log](#-$-git-log) |
| merge | ㅇ | [merge](#-$-git-merge-/-$-git-rebase) |
| pull | ㅇ | [pull](#-$-git-push-/-$-git-clone-/-$-git-pull) |
| push | ㅇ | [push](#-$-git-push-/-$-git-clone-/-$-git-pull) |
| rebase | ㅇ |  [rebase](#-$-git-merge-/-$-git-rebase) |
| remote |ㅇ |  [remote](#-GitHub에-문서-업로드하기-/-$-git-remote) |
| reset --hard | ㅇ | [reset --hard](#-$-git-reset---hard) |
| status | ㅇ| [status](#-$-git-add-/-$-git-commit-/-$-git-status) |
| tag |ㅇ| [tag](#-$-git-tag) |
