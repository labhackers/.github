# 🔐 [LABHACKER'S SECURITY POLICY](#toc)

> 👉 This file is included by default with all `LabHacker's` repositories by virtue of its inclusion in the [`.github`](https://github.com/ragdata/.github) repository, which defines defaults for all other repositories under an organisation.
>
> `LabHacker's Security Policy v-1.0.0`

#### This document outlines the security policies and default procedures for all projects I initiate.

<details>
<summary><a name="toc" href="#toc"><h2>📖 Index / Table of Contents</h2></a></summary>

- [SECURITY POLICIES](#-security-policy)
	- [Supported Versions](#supported-versions)
	- [Reporting an Issue](#-reporting-an-issue)
	- [Disclosure Policy](#-disclosure-policy)
	- [Scope of Policy](#-scope-of-policy)
	- [A Word About 'Bug Bounties'](#-a-word-about--bug-bounties-)
	- [Security Advisories](#-security-advisories)
	- [Comments on this Policy](#-comments-on-this-policy)

</details>

## [Supported Versions](#toc)

The current supported version of Bash Bits is: [**v-1.0.0**]()

## 🐞 [Reporting an Issue](#toc)

I, and those I choose to collaborate with, take all bugs very seriously.  We know all too well how much damage even the most innocent-looking bugs can cause if exploited with malicious intent.  Because of the seriousness of these matters, we very much appreciate your efforts and your responsible disclosure.  In return, we will make every effort to acknowledge your contribution.

Please report all bugs using the Issue Tracker available for each organisation and as a part of every repository.

When reporting a bug, the following is some of the information you might think to include:

- The website, page or repository where the bug may be observed
- A brief description of the bug
- Optionally, the type of vulnerability and OWASP Category, if applicable
- As many details as you can provide without risking further distribution of the exploit

Your submission will be acknowledged within 48 hours, and a more detailed response will follow which indicates the steps we intend to take next in handling your report.  After the initial reply to your report, the security team will endeavour to keep you informed of the progress of the fix and the timing of the public announcement, and may ask for additional information or guidance from you if we need it.

Please report bugs discovered in any third-party modules to the person or team maintaining that module.  It is neither within our power or our purview to fix bugs in code that we are not responsible for maintaining.

<h4 align="center">
<a href="https://github.com/labhackers/cookbook/issues">Please report low-level bugs using the Issue Tracker</a>
<br><br>
<a href="mailto:security@ragdata.dev?subject=LabHackers%20Security%20Report">For more serious issues, please report via email to security@ragdata.dev</a>
</h4>

## 📃 [Disclosure Policy](#toc)

When the security team receives a bug report, it is assigned to a primary handler.  This person will coordinate the fix and release process, and this involves the following steps:

- Confirm the bug and determine the affected versions
- Audit code to find any potential similar problems
- Prepare fixes for all releases still under maintenance

## 🚫 [Scope of Policy](#toc)

The following are NOT in the scope of this policy:

- volumetric vulnerabilities - for example, overwhelming a service with a high volume of requests;
- reports indicating that our services do not fully align with 'best practices' according to one body or another;
	- (ie: the latest opinions of one outspoken "thought leader" or another neither concern nor impress me)


## 💰 [A Word About "Bug Bounties"](#toc)

> (the opinion of one outspoken and internationally ignored "thought leader")
>
> Unfortunately, I have not yet made my fortune out of software - although that is most certainly still my intention - so I do not currently offer a paid "Bug Bounty" program.  I'm just some random bloke like any other trying to scratch out a living using his meagre wit and talents.  If I do suddenly stumble upon that elusive something which proves to be the basis upon which I may build a fortune, then this will likely change - until then, however, we (being myself and those I may have chosen to collaborate with) will make every effort to show our appreciation to the people who generously give their time and make the effort to expose vulnerabilities in our code in a responsible, discreet manner, and reserve our everlasting disdain for those who do otherwise - including those withholding information in the hope of or while demanding monetary reward in exchange.  I believe it is ENTIRELY in opposition to the fundamental principles of open-source software for this sort of practice to be engaged in, and will not beat about the bush before telling anyone who inquires about such exactly where they can find their "Bug Bounty", and when they can expect to receive it.

## 📣 [Security Advisories](#toc)

We will pass on to consumers of our products any and all security advisories that we may receive with regard to any third-party application that is distributed as one of our projects in a timely manner, and will attempt to do the same with any patches and upgrades which may follow as a result of an advisory we've received.  If the vulnerability is severe enough, and a patch or upgrade does not appear to be on its way from the maintainer of the package(s) involved, we will not hesitate to remove that package from our distribution and either replace it immediately, or do without until a suitable replacement can be found.

At no point will we - through neglect or omission - put the security of our customer's devices at risk in favour of saving face.  We will be frank and honest with regard to the extent and severity of all security incidents as news of them comes to hand, and this will remain a primary concern for us until the day we cease operations.

## 💬 [Comments on This Policy](#toc)

If you have any comments on how this policy might be improved, please don't hesitate to get in touch - you can find a list of places you might be able to do that in our [**Community Support Document**][SUPPORT].

[SUPPORT]: https://github.com/labhackers/.github/blob/master/.github/SUPPORT.md
