# ashley's `/git(hub)?/g` convention

Progress:
- [ ] commiting guide
- [ ] commit message convention
- [ ] branch naming scheme
- [ ] pr naming scheme
- [ ] github flow description
- [ ] how to prs guide
- [ ] how to issues guide
- [ ] why you should use the `github issue notebooks` vscode extension
- [ ] gh cli guide

## Table Of Contents



## commiting guide: `atomic commits`


## commit message convention: `hrcc`


## branch naming scheme: `hrbc`


## pr naming scheme: `hrpr`

---
---
## github flow description

Github Flow is a lightweight, branch-based git workflow.

The main concepts I will be adressing here are these:

- the main (prod) branch
- the dev (develop) branch
- feature branches
- hotfix branches
- why we use squash when we do feature -> dev prs
- why we use merge when we use dev -> main prs

---
### main branch

the main branch in a github flow repository is `main`. it could also be called `master`, `trunk`, etc.

this branch is best described as the *production* branch.

whenever you make a pr from dev (main development branch) to this branch, you are essentially releasing a new version of your software.

what a version means is up to you.

whenever you release a new version, you tag it (`git tag` or github's web ui).

tagging also allows for easy CD.

---

### dev branch

the dev branch in a github flow repository is usually `dev`. it could also be called `develop`, `development`, `devel`, among other things.

this branch is best described as *the latest development version*.

all feature branches eventually end up squashed into here.

this is the only branch besides `main` who has `hrcc` commit histories.

this is also the only branch allowed to be merged into `main`.

---

### feature branches

these branches are the *pr branches*.

basically, these branches are the `from` in `from -> to`, where `to` is always `dev`.

the commits on these branches do not have to follow the `hrcc`, because when these are squash-commited, it will provide `hrcc` commits to the actual branches that have changelogs.

these branches are allowed allow to be squashed, and only into `dev`.

---
### hotfix branches

these branches are the branches that are used to fix important issues in the `main` branch.

essentially, if you accidentally push a very severe bug to `main`, you would use a hotfix branch in order to fix it.

a small explanatoin of a hotfix workflow:

- created off latest `main`
- only commits allowed on hotfix are about issue
- no feature enhancements or chores (`feat` or `chore` in *`hrcc`*)
- merges into both master & develop branches when its finished
- deleted after merge

---
### why squash for feature -> dev?


---
### why merge for dev -> main?


---
---

## how to prs guide


## how to issues guide


## why you should use the `github issue notebooks` vscode extension


## gh cli guide
