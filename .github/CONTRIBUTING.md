# 📑 [LabHacker's Contributor's Guide](#toc)

> 👉 This file is included by default with all `LabHacker's` repositories by virtue of its inclusion in the [`.github`](https://github.com/ragdata/.github) repository, which defines defaults for all other repositories under an organisation.
>
> `LabHacker's Contributor's Guide v-1.0.1`

Firstly, I'd like to thank you personally for taking the time to help improve this project, I truly appreciate it! 💓 Here are a few guidelines to help ensure that all contributions are heading in the same direction:

You can contribute by:

- giving the project a star ⭐
- responding to issues
- [sponsor me on GitHub][sponsorship]
- [sponsor me on Ko-Fi][ko-fi]
- supporting me through one of my social channels (see [SUPPORT][support])

<details>
<summary><h2><a name="toc" href="#toc">📖 Index / Table of Contents</a></h2></summary>

- [Contributor's Guide](#-contributors-guide)
  - [NON-CODE CONTRIBUTIONS](#-non-code-contributions) 
  - [Standards](#-standards)
    - [Versioning Standards](#-versioning-standards)
    - [VCS Standards](#-vcs-standards)
    - [Code Stability](#-code-stability)
  - [Tools](#-tools)
    - [GitHub](#-octocat--github)
    - [Reusable Workflows](#-reusable-workflows)
    - [Release Manager](#-release-manager)
    - [Bash-Bits](#-bash-bits)
  - [Basic Process for Pull Requests](#-basic-process-for-pull-requests)
  - [Verify Your Commit Messages!](#-verify-your-commit-messages-)
    - [Valid Commit Types](#-valid-commit-types)
    - [Valid Commit Message Structure](#-valid-commit-message-structure)
    - [RULES](#-rules)
    - [Examples](#-examples)
  - [Remember Always](#-remember-always-)

</details>

## 💡 [NON-CODE CONTRIBUTIONS](#toc)

To make a contribution which will be recognised on the appropriate `CONTRIBUTORS` page, submit a `contribution` issue to the appropriate repository's issue register.  Once it has been reviewed and accepted, your contribution will be recorded on the appropriate `CONTRIBUTORS` page.  More significant contributions may be recognised elsewhere in relation to the project as well.

The recognition of Non-Code Contributions are made possible by the [All-Contributors](https://allcontributors.org) bot. 

[`^ Top`](#toc)

## 🌟 [Standards](#toc)

All of my projects employ the following standard procedures for code production and management.  Please be aware that failure to adhere to the following standards may see your contributions excluded from the project.

[`^ Top`](#toc)

### 💞 [Versioning Standards](#toc)

All of my projects use [**Semantic Versioning 2.0.0 (SemVer)**][semver].  Briefly:

1. **MAJOR** version increments when you make a _breaking change_ (ie _NOT backwards compatible_)
2. **MINOR** version increments when you add functionality which _IS backwards compatible_
3. **PATCH** version increments whenever you make _minor backwards compatible releases_ such as bugfixes

Adding a new feature will generally cause either the PATCH or MINOR version to increment, depending upon the extent of the feature.

[`^ Top`](#toc)

### 🚧 [VCS Standards](#toc)

- The version control system I employ is [Git][git] with remote repositories hosted by [GitHub][github].
- All git commit messages must be compliant with the [**Conventional Commits Guidelines**][conventional-commits]
	- you can find out more about conventional commits [below](#valid-commit-types)
- Branches are organised according to the [**Gitflow Workflow**][gitflow]
	- branches you will encounter:
      - `master` - the latest supported codebase
      - `develop` - code under development
      - `feature/feature-name` - specific feature branch
      - `hotfix/name` or `hotfix/issue-number` - specific hotfix branch
      - `release/version` - specific release / tag branch
      - `gh-pages/*` - branch containing the project's GitHub Pages (Jekyll) Website
	  - `pkg/*` - branch containing a public docker package
      - `env/*` - branch containing a dockerized development environment (private docker package)
<br /><br />
	- the default branch for any repository is always `master`
	- development work is conducted either in the `develop` branch, or a `feature` branch
      - a feature branch name always takes the form: `feature/feature-name`
	- bugfixes (generally work conducted in response to a raised issue) are conducted in branches with a name of the form: `hotfix/name` or `hotfix/issue-number`
	- releases are compiled in a release branch with a name of the form: `release/version`
      - release branches are almost always deleted as soon as the release goes live
<br /><br />
- Repositories with an associated GitHub Pages Project Website will contain branches with names starting with `gh-pages/`
	- the `gh-pages/` branches follow a similar format for development and releases:
      - `gh-pages/master`
      - `gh-pages/develop`
      - `gh-pages/feature/name`
      - `gh-pages/hotfix/issue-number`
      - `gh-pages/release/version`

[`^ Top`](#toc)

### 🚥 [Code Stability](#toc)

With reference to the VCS Standard above, code stability is generally like so:

| Branch               |      Stability       | Code Age         | Reliability |
|----------------------|:--------------------:|------------------|:-----------:|
| `master`             |    latest stable     | latest release   |     🟢      |
| `develop`            |   latest unstable    | most recent code |     🔴      |
| `feature/*`          |       unstable       | unpredictable    |     🔴      |
| `hotfix/*`           |       unstable       | unpredictable    |     🔴      |
| `release/*`          |        stable        | tagged versions  |     🟡      |
| `gh-pages/master`    |    latest stable     | latest release   |     🟢      |
| `gh-pages/develop`   |   latest unstable    | most recent code |     🔴      |
| `gh-pages/release/*` |        stable        | tagged versions  |     🟡      |
| `pkg/name/master`    |    latest stable     | latest release   |     🟢      |
| `pkg/name/develop`   |   latest unstable    | most recent code |     🔴      |
| `pkg/name/release/*` |        stable        | tagged versions  |     🟡      |
| `env/name`           | perpetually unstable | most recent code |     🔴      |

[`^ Top`](#toc)

## 🔨 [Tools](#toc)

I like to put my money where my mouth is and demonstrate confidence in my own work, therefore, wherever possible, my GitHub repositories will include some of my other repositories as either a submodule or a few essential files.  The most common of these being:

###  :octocat: [.github](https://github.com/ragdata/.github)

> 💡 **DID YOU KNOW?** If you include a repository for your GitHub Account or Organization called `.github`, the files that you include in **its** `.github/` directory will serve as the defaults for ALL other repositories under that account or organization.

The ['community standards'](https://github.com/Ragdata/.github/community) files utilized by ALL of my repositories ALL come from this one project.  If any repository has need of a custom version of one of these files, it gets it, otherwise you can find all the default versions here.

### ⚡ [Reusable Workflows](https://github.com/ragdata/workflows)

> 💡 **DID YOU KNOW?** You don't **_have_** to use a GitHub Action from the marketplace in your GitHub workflows - you can just as effectively use a file from one of your own repositories!

All the GitHub actions and associated workflows I use in all of my repositories live here.  This allows me to create workflows which are tailored specifically for _my_ code, and are a lot lighter than generic actions.  I've left this as a public repo so that you can study the techniques used and implement them for yourself!

[//]: # (### 🎁 [Release Manager]&#40;https://github.com/ragdata/release-manager&#41;)

[//]: # ()
[//]: # (I include a configuration file &#40;`.releaserc`&#41; for `Release Manager` in every single one of my repositories.  It takes care of writing my CHANGELOGS, incrementing versions recorded throughout my repositories and ensures that my releases are orderly and compliant with [semantic versioning][semver].  `Release Manager` can be used from the Linux command line, or as part of a GitHub workflow!)

[//]: # ()
[//]: # (### 🧩 [Bash Bits]&#40;https://github.com/ragdata/bash-bits&#41;)

[//]: # ()
[//]: # (`Bash Bits` is my modular library for Bash.  Because a fair amount of the stuff I write is written for the Linux command line, `Bash Bits` ends up finding a place in most of my repositories, and if you're writing for Bash, it could be a valuable part of one of yours too!  `BB` is unique in that it is written particularly with users of WSL2 &#40;Ubuntu&#41; in mind!)

[`^ Top`](#toc)

## ✂️ [Basic Process for Pull Requests](#toc)

Generally, the way to create a **Pull Request** is to:

1. Fork this project and clone it locally
2. Create a new branch from the master branch and give it a descriptive name followed by the issue number, if applicable (format: `feature/<new feature> [#issue]` or `fix:<bug> [#issue]`)
3. AFTER completing development AND TESTING, submit a new _Pull Request_
	1. (note that your commit message MUST follow the [Conventional Commits Guidelines][conventional-commits], otherwise it will fail the PR check)

[`^ Top`](#toc)

## 🔍 [Verify Your Commit Messages!](#toc)

If you want to make sure your commit messages will pass the CI check, implement the following:

### 📝 [Valid Commit Types](#toc)

- build
- chore
- ci
- docs
- feat
- fix
- perf
- refactor
- revert
- style
- test

[`^ Top`](#toc)

### 📜 [Valid Commit Message Structure](#toc)

```console
<type>(optional scope): <subject>

<optional body>

<optional footer>
```

[`^ Top`](#toc)

### 📑 [RULES](#toc)

- Type **MUST** be one of those in the list above
- Type **MUST** be all lowercase
- Type **CANNOT** be empty


- Subject **MUST** start with a lowercase letter
- Subject **CANNOT** be empty
- Subject **CANNOT** end in a period


- Max length of `<type>(scope): <subject>` is 100 chars


- Body **MUST** be preceded by a blank line
- Max length of body is 100 chars **PER LINE**


- Footer **MUST** be preceded by a blank line
- Max length of footer is 100 chars **PER LINE**

[`^ Top`](#toc)

### 💼 [Examples](#toc)

#### Commit message with description and BREAKING CHANGE footer:
```
feat: allow provided config object to extend other configs

BREAKING CHANGE: `extends` key in config file is now used for
extending other config files
```
#### Commit message with `!` to draw attention to breaking change:
```
feat!: send an email to the customer when a product is shipped
```
#### Commit message with scope and `!` to draw attention to breaking change:
```
feat(api)!: send an email to the customer when a product is shipped
```
#### Commit message with both `!` and BREAKING CHANGE footer
```
chore!: drop support for Node 6

BREAKING CHANGE: use Javascript features not available in Node 6
```
#### Commit message with no body
```
docs: correct spelling of CHANGELOG
```
#### Commit message with scope
```
feat(lang): add Polish language
```
#### Commit message with multi-paragraph body and multiple footers
```
fix: prevent racing of requests

Introduce a request id and a reference to latest request.
Dismiss incoming responses other than from latest request.

Remove timeouts which were used to mitigate the racing issue
but are obsolete now.

Reviewed-by: Z
Refs: #123
```

### 📌 [Remember Always:](#toc)

> _We see much further, and reach much higher, only because we stand upon the shoulders of giants_

:tada: **THANK YOU** :tada:

[`^ Top`](#toc)

[sponsorship]: https://github.com/sponsors/Ragdata
[ko-fi]: https://ko-fi.com/ragdata
[support]: https://github.com/labhackers/.github/blob/master/.github/SUPPORT.md
[conventional-commits]: https://www.conventionalcommits.org/en/v1.0.0/
[git]: https://git-scm.com/
[github]: https://github.com
[gitflow]: https://nvie.com/posts/a-successful-git-branching-model
[semver]: https://semver.org/
