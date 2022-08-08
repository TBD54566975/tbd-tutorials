# Contribution Guide 

There are many ways to be an open source contributor, and we're here to help you on your way! You may:

* Propose ideas in our 
  [discussion forums](https://forums.tbd.website)
* Raise an issue or feature request in our
  [issue tracker](https://github.com/TBD54566975/tbd-tutorials/issues)
* Help another contributor with one of their questions, or a code review
* Suggest improvements to our Getting Started documentation by supplying a Pull Request
* Evangelize our work together in conferences, podcasts, and social media spaces.

This guide is for you.

## Development Prerequisites

| Requirement                     | Tested Version  | Installation Instructions                                                                                    |
|---------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------|
| Java                            | 18.0.2          | Below, recommended via [SDKMan](https://sdkman.io)                                                           |
| [JBang](https://www.jbang.dev/) | 0.96.4          | Below, recommended via [SDKMan](https://sdkman.io)                                                           |
| Gitdown                         | 3.1.5           | `npm install gitdown -g`, requires `npm` installation recommended via [`nvm`](https://github.com/nvm-sh/nvm) |
| Docker Engine and Compose       | 19.03.8 (Linux) | Below, or via [Docker Desktop](https://docs.docker.com/desktop/#download-and-install)                        |

### Java and JBang

This project's build system uses Java, a typesafe, compiled programming language. 

You may verify your `java` installation via the terminal by running `java -version`.

If you do not have Java, we recommend installing it 
via [SDKMan](https://sdkman.io/install). This is a project which will allow you 
to easily install the Java Development Kit (JDK), runtime (JRE), and related frameworks, 
build tools, and runtimes.

After you've installed SDKMan, you may install Java:

#### SDKMan (cross-platform instructions)

```shell
$> sdk install java 
 ...
Do you want java 18.0.2-open to be set as default? (Y/n): Y
Setting java 18.0.2-open as default.
```

You may test your installation:

```shell
$> java -version
openjdk version "18.0.2" 2022-07-19
OpenJDK Runtime Environment (build 18.0.2+9-61)
OpenJDK 64-Bit Server VM (build 18.0.2+9-61, mixed mode, sharing)
```

#### JBang

JBang brings the power of Java to scripting. It's how we automate the tutorials and run
the test suites. It can be installed from the [JBang site](https://www.jbang.dev/download/)
or through SDKMan, as recommended above for Java:

```shell
$> sdk install jbang
```

You may verify your installation:

```shell
$> jbang --version
0.96.4
```

### Docker Engine and Compose Plugin

Many of our services are built and run as containerized applications in the Docker format. 

#### Mac and Windows Users

You'll likely get everything you need from the Docker ecosystem via 
installation of Docker Desktop.

* [macOS Intel](https://docs.docker.com/desktop/install/mac-install/)
* [macOS Apple Silicon](https://docs.docker.com/desktop/mac/apple-silicon/)
* [Windows](https://docs.docker.com/desktop/install/windows-install/)

#### Linux

Linux users may also 
[install Docker Engine and the Compose Plugin](https://docs.docker.com/desktop/install/linux-install/) 
via Docker Desktop, or through 
[adding the Docker repositories](https://docs.docker.com/engine/install/fedora/#set-up-the-repository) and
installing via tools like Fedora's `dnf`:

```shell
$> sudo dnf -y install dnf-plugins-core
$> sudo dnf config-manager \
    --add-repo \
    https://download.docker.com/linux/fedora/docker-ce.repo
$> sudo dnf install docker-ce docker-ce-cli containerd.io docker-compose
```

You can validate that you have Docker installed:

```shell
$> docker help
```

You may want to run the 
[Linux Docker postinstall steps](https://docs.docker.com/engine/install/linux-postinstall/)
to run Docker as non-root.

#### All Platforms

Test Docker is running and working:

```shell
$> docker run hello-world
```

## Build (JBang)



## Communications

### Issues

Anyone from the community is welcome (and encouraged!) to raise issues 
via [GitHub Issues](https://github.com/TBD54566975/tbd-tutorials/issues).

### Forums

Design discussions and proposals take place on our 
[Discourse Forums](https://forums.tbd.website/) .

We advocate an asynchronous, written debate model - so write up your thoughts and 
invite the community to join in!

### Continuous Integration

TBD.

## Contribution

We review contributions to the codebase via GitHub's Pull Request mechanism. We have 
the following guidelines to ease your experience and help our leads respond quickly 
to your valuable work:

* Start by proposing a change either in Issues (most appropriate for small 
  change requests or bug fixes) or in Discussions (most appropriate for design 
  and architecture considerations, proposing a new feature, or where you'd 
  like insight and feedback)
* Cultivate consensus around your ideas; the project leads will help you 
  pre-flight how beneficial the proposal might be to the project. Developing early 
  buy-in will help others understand what you're looking to do, and give you a 
  greater chance of your contributions making it into the codebase! No one wants to 
  see work done in an area that's unlikely to be incorporated into the codebase.
* Fork the repo into your own namespace/remote
* Work in a dedicated feature branch. Atlassian wrote a great 
  [description of this workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow)
* When you're ready to offer your work to the project, first:
* Squash your commits into a single one (or an appropriate small number of commits), and 
  rebase atop the upstream `main` branch. This will limit the potential for merge 
  conflicts during review, and helps keep the audit trail clean. A good writeup for 
  how this is done is 
  [here](https://medium.com/@slamflipstrom/a-beginners-guide-to-squashing-commits-with-git-rebase-8185cf6e62ec), and if you're having trouble - feel free to ask a member or the community for help or leave the commits as-is, and flag that you'd like rebasing assistance in your PR! We're here to support you.
* Open a PR in the project to bring in the code from your feature branch.
* The maintainers noted in the `CODEOWNERS` file will review your PR and optionally 
  open a discussion about its contents before moving forward.
* Remain responsive to follow-up questions, be open to making requested changes, and...
  You're a contributor!
* And remember to respect everyone in our global development community. Guidelines 
  are established in our `CODE_OF_CONDUCT.md`.