---
marp: true
---


# Shell, vim command for git

## Fastcampus Programming SCHOOL

---

<!--
paginate: true
theme: default
size: 16:9
footer : fastcampus, Wooyoung Choi, 2020
-->

## 최우영

- Co-founder, CTO(disceptio)
- Solution Architect, Web Developer, Instructor
- Skills: Python, Golang, Julia, Node.js, Google tag manager ...

### Contacts

1. blog: https://ulgoon.github.io/
2. github: https://github.com/ulgoon/
3. email: me@ulgoon.com
4. discord: @ulgoon

---

## Introduce

---

## Goal(1)

- Linux의 역사를 이해한다
- CLI에 대한 공포를 극복하고 Shell과 친구가 된다
- Linux Shell 커맨드를 학습하여 능숙하게 이를 활용할 수 있다
- Vim 텍스트 에디터를 이용하여 커밋메시지를 작성하고, 파일 수정을 할 수 있다

---

## Goal(2)

- git을 이해하고, git과 github이 다름을 인지한다
- git을 활용하여 나의 소스코드를 관리할 수 있다
- 나의 커리어를 Swag 할 수 있는 블로그를 git을 활용하여 관리할 수 있다.
- git의 branch model을 활용해 능숙하게 코드관리할 수 있다
- git으로 타인과 협업하며, 다른 프로젝트에 기여할 수 있다

---

## Contents

- Introduction to Linux, Shell
- Shell commands
- Vim commands

---

## Before Linux(1)

![](http://www.unix.org/u30logo/unix_logo.gif)

- 1965년 데니스 리치, 켄 톰슨 외 x명이 AT&T Bell 연구소에서 PDP-7 기반 어셈블리어로 작성한 UNIX를 개발

---

## Before Linux(2)

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/46/Ken_Thompson_and_Dennis_Ritchie.jpg/270px-Ken_Thompson_and_Dennis_Ritchie.jpg)

- 1973년 데니스 리치와 켄 톰슨이 C를 개발한 뒤, C 기반 UNIX 재작성

---

## Before Linux(3)

![](http://i1-news.softpedia-static.com/images/news2/Richard-Stallman-Says-He-Created-GNU-Which-Is-Called-Often-Linux-482416-2.jpg)
- 1984년 리차드 스톨먼이 오픈 소프트웨어 자유성 확보를 위한 GNU 프로젝트 돌입

---

### Meaning of GNU

GNU == `G`NU is `N`ot `U`nix

---

## Before Linux(4)

![](http://i.imgur.com/SMYPY.jpg)

- But, GNU 프로젝트에는 커널이 없었고..

---

### Kernel

![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8f/Kernel_Layout.svg/380px-Kernel_Layout.svg.png)

- 하드웨어와 응용프로그램을 이어주는 운영체제의 핵심 시스템소프트웨어

---

## Linus Torvalds

https://www.youtube.com/embed/IVpOyKCNZYw

- 헬싱키 대학생이던 리누스 토발즈는 앤디 타넨바움의 MINIX를 개조한 Linux를 발표
- 0.1 - bash(GNU Bourne Again SHell), gcc(UNIX 기반 C 컴파일러)

---

## Linux

- 리누스 토발즈가 작성한 커널 혹은 GNU 프로젝트의 라이브러리와 도구가 포함된 운영체제
- PC와 모바일, 서버, 임베디드 시스템 등 다양한 분야에서 활용
- Redhat, Debian, Ubuntu, Android 등 다양한 배포판이 존재

---

## Shell

- 운영체제의 커널과 사용자를 이어주는 소프트웨어

- sh(Bourne Shell): AT&T Bell 연구소의 Steve Bourne이 작성한 유닉스 쉘
- csh: 버클리의 Bill Joy가 작성한 유닉스 쉘(C언어랑 비슷한 모양)
- bash(Bourne Again Shell): Brian Fox가 작성한 유닉스 쉘
	- 다양한 운영체제에서 기본 쉘로 채택
- zsh: Paul Falstad가 작성한 유닉스 쉘
	- sh 확장형 쉘
	- 현재까지 가장 완벽한 쉘

---

## Let's learn bash

---

## Shell Command Basic(1)

```shell
$ cd documents

$ mkdir dev # - make directory dev
$ cd dev # - change directory
$ cd .. # - go up
$ pwd # - print working directory

$ ls
$ ls -al

$ touch hello.py # - create hello.py
$ exit # - terminate shell
```

---

## chmod

> 파일의 권한을 설정할 때 사용

`drwxr-xr-x`
`d` or `-`: directory or file
(user)(group)(other)
`r`: read
`w`: write
`x`: execute
`-`: no permission

---

## chmod

`$ chmod [옵션] (8진수) (파일명)`
8진수
0: 000
1: 001
2: 010
3: 011
4: 100
5: 101
6: 110
7: 111

---

## Shell Command Basic(2)

```shell
$ mv hello.py dev
$ cp hello.py dev

$ rm hello.py
$ rm -rf dev/

$ cat README.md
$ head README.md
$ tail -20 README.md
$ cat README.md > README.txt
$ open README.md # use explorer instead open on windows
```

---

## Vim

![](https://www.vim.sexy/img/Vimlogo.svg)

---

# TODO

1. documents/dev에서 fastcampus 디렉토리를 만듭니다
2. 새파일 index.html을 만들어주세요
3. vim으로 내부 작업을 한뒤 저장하여 cat 명령어로 저장을 확인합니다.
4. index.html을 style.css로 이름을 변경합니다.

---

![height:600px](https://kldp.org/files/vi-vim-cheat-sheet-ko.png)

---

## Vim Basic

`h,j,k,l - move cursor`
`i - insert mode`
`v - visual mode`
`d - delete`
`y - yank`
`p - paste`
`u - undo`
`r - replace`
`$ - move end of line`
`^ - move start of line`
`:q - quit`
`:q! - quit w/o write(no warning)`
`:wq - write and quit`
`:{number} - move to {number}th line`

---

### write `hello.py` with Vim

`$ vim`
`$ vim hello.py`

`i`
`-- insert --`
type `print("hello python!")`
press `esc` to escape

`:wq`

`$ python hello.py`

---

### copy & paste

`$ vim hello.py`

`v`
`-- visual --`
블록지정 후 `y`
`p`

press `esc` to escape
`:wq`

`$ python hello.py`

---

### Use Vim in real world!

- [vim advanture](https://vim-adventures.com/)
- [vimium](https://chrome.google.com/webstore/detail/vimium/dbepggeogbaibhgnhhndojpepiihcmeb?hl=en)
- [vs code vim](https://github.com/VSCodeVim/Vim)

<link href="https://fonts.googleapis.com/css?family=Nanum+Gothic:400,800" rel="stylesheet">
<link rel='stylesheet' href='//cdn.jsdelivr.net/npm/hack-font@3.3.0/build/web/hack-subset.css'>

<style>
h1,h2,h3,h4,h5,h6,
p,li, dd, table > * > * {
font-family: 'Nanum Gothic', Gothic;
}
span, pre {
font-family: 'Hack', monospace;
}
</style>