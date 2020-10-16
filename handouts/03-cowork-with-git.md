---
marp: true
---


# git (2)

## Fastcampus Programming SCHOOL

---

<!--
paginate: true
theme: default
size: 16:9
footer : fastcampus, Wooyoung Choi, 2020
-->

## Branch

---

## What is branch?

---

## What is branch?(1)

![height:500px](https://www.sideshowtoy.com/assets/products/3005011-groot/lg/marvel-guardians-of-the-galaxy-groot-premium-format-3005011-02.jpg)

---

## What is branch?(2)

분기점을 생성하고 독립적으로 코드를 변경할 수 있도록 도와주는 모델

ex)

master branch

```python
print('hello world!')
```

another branch

```python
for i in range(1,10):
    print('hello world for the %s times!' % i)
```

---

## Branch(1)

Show available local branch
`$ git branch`

Show available remote branch
`$ git branch -r`

Show available All branch
`$ git branch -a`

---

## Branch(2)

Create branch
`$ git branch stem`

Checkout branch
`$ git checkout stem`

Create & Checkout branch
`$ git checkout -b new-stem`

make changes inside readme.md
`$ git commit -a -m 'edit readme.md'`
`$ git checkout master`

merge branch
`$ git merge stem`

---

## Branch(3)

delete branch
`$ git branch -D stem`

push with specified remote branch
`$ git push origin stem`

see the difference between two branches
`$ git diff master stem`

---

## Branch asciinema

[![asciicast height:400px](https://asciinema.org/a/qRmUXvtrkXS6Y09H9TM1hVAhT.svg)](https://asciinema.org/a/qRmUXvtrkXS6Y09H9TM1hVAhT)

---

## branching models

- git flow
  - (hotfix)- `master` -(release)- `develop` - feature
  - pros: 가장 많이 적용, 각 단계가 명확히 구분
  - cons: 복잡..
- github flow
  - `master` - feature
  - pros: 브랜치 모델 단순화, `master`의 모든 커밋은 deployable
  - cons: CI 의존성 높음. 누구 하나라도 실수했다간..(pull request로 방지)
- gitlab flow
  - `production` - `pre-production` - `master` - feature
  - pros: deploy, issue에 대한 대응이 가능하도록 보완
  - cons: git flow와 반대 (`master`-develop, `production`-master)

---

## git flow strategy

![](https://b.kisscc0.com/20180815/saq/kisscc0-github-branching-workflow-diagram-1492474981-svg-5b74286bb0f1a7.6096632915343391797248.png)

---

## use git flow easily!

[Link](https://danielkummer.github.io/git-flow-cheatsheet/index.ko_KR.html)

![](https://danielkummer.github.io/git-flow-cheatsheet/img/git-flow-commands.png)

---

## Collaborate with your Co-worker

---

## Method 1: Collaboration

Add Collaborator
![](../img/collaborators.png)

---

## Collaboration

Add, Commit and Push like you own it. 

---

## Method 2: Fork and Merge

![](../img/fork1.png)

---

## Fork and Merge

![](../img/fork2.png)

---

## Fork and Merge

![](../img/fork3.png)

---

## Fork and Merge

`$ git clone https://github.com/username/forked-repo.git`

---

## Fork and Merge

`$ git branch -a`
`$ git checkout -b new-feature`

---

## Fork and Merge

Make some change

`$ git add file`
`$ git commit -m "commit message"`
`$ git push origin new-feature`

---

## Fork and Merge

![](../img/pr1.png)

---

## Fork and Merge

![](../img/pr2.png)

---

## Fork and Merge

![](../img/pr3.png)

---

## Fork and Merge

![](../img/pr4.png)

---

## Fork and Merge

![](../img/pr5.png)

---

## Fork and Merge

![](../img/pr6.png)

---

## Fork and Merge

![](../img/pr7.png)

---

1. 팀장이 자기 소유의 repo를 만든다
2. clone 하여 약간의 작업 후 add, commit, push
3. notice 받은 팀원은 fork 하여 자신의 소유가 된 repo를 clone
4. 작업할 내용을 미리 issue 등록
4-1. or 팀장이 강제 issue 생성 후 작업지시 
5. `$ git remote add pmorigin {pm의 repo 주소}` 하여 미리 등록
6. feature branch 생성 후 작업, add, commit(with issue no)
7. master로 merge 한 후, 나의 master로 push
8. pull request 생성
9. 팀장은 확인 후 merge(conflict, file change 확인 필수)

---

## volvocars main page clone with git flow

1. role 분배(40분안에 클론하려면 어떻게 역할을 나눠야 할까)
2. 위의 과정 반복

---

## continuous pull

---

## continuous pull

`$ git remote add upstream https://github.com/anotheruser/original-repo.git`

`$ git fetch upstream`
`$ git merge upstream/master`

---

## How to move files

### Don't

```shell
$ mv style.css static/css
```
-> deleted:
-> untracked files:

### Do

```shell
$ git mv style.css static/css
```
-> renamed:

---

## Issue & Projects

Issue: 프로젝트, 레포와 관계된 모든 해야할 일과 버그, 개선사항 등을 기록

Projects: 해야할 일의 진도에 따른 구성과 우선순위 지정

---

### Issue(1)

![height:400px](../img/issue1.png)

---

### Issue(2)

![height:400px](../img/issue2.png)

---

### Issue(3-1)

![height:550px](../img/issue3.png)

---

### Issue(3-2)

- Assignees: 이 이슈에 대한 책임인원
- Labels: 이슈의 종류
- Projects: 이슈를 배당할 프로젝트
- Milestone: 이슈에 해당하는 중요 시점 지정

---

### Projects

---

### Projects(2)

![](../img/projects1.png)

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