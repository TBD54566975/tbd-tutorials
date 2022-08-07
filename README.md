# TBD Tutorials and Examples
This repository is a prototype collection of examples and 
tutorials using TBD frameworks, SDKs, and services. It's a place for the 
community to contribute ideas demonstrating concepts provided by TBD APIs. 
The goal here is to give our tutorials and examples a common format, enabling 
us to:

* Publish tutorials and examples as documentation on 
  [developer.tbd.website](developer.tbd.website).
* Test example code in CI to ensure it
  remains runnable as development progresses
* Highlight the community authors who contributed the example
* Build a deep knowledge base over time
* Give developers a starting point for their own innovation

## Tutorials and Examples Format
_This section is a draft open to suggestions and modifications._

Each example/tutorial will likely contain the following components:

* Documentation
* Code
* Tests

The motivation for this work stemmed from Frank Hinek's [excellent 
blog post](https://frankhinek.com/getting-started-with-tbds-ssi-service/) 
highlighting early usage of the SSI Service. We asked ourselves: what if this
could be tested, publishable, and repeatable for other use cases? Thus his 
example becomes a nice testing ground to port into a common format and build
system we define here.

## Running the Build

---

The build for these tutorials and examples does two things:

* Creates the unified Markdown docs from the snippits and fragments
* Runs the tests (NOT YET IMPLEMENTED).

Right now there's no build script; the build is done through the CLI in the commands below.
When done prototyping we can make a build system for this.

**NOTE**

IDK man, Pandoc can't seem to create directories (or files when running 
it in Docker mode). So we create the output directory via `mkdir` or similar depending on your system,
, and i'll be cool to not have to make users install Pandoc 
on their system by running it via Docker which is already a prereq. - ALR

---

### Script to run build via Docker
```shell

$> mkdir build
$> touch build/GETTING_STARTED_SSI_SERVICE.md 
$> docker run --rm --volume "`pwd`:/data" --user `id -u`:`id -g` pandoc/core:2.19.0.0 getting-started-ssi-service/GETTING_STARTED_SSI_SERVICE.md -o build/GETTING_STARTED_SSI_SERVICE.md
```


### Script to run build via Pandoc on system
```shell
$> mkdir build
$> pandoc getting-started-ssi-service/GETTING_STARTED_SSI_SERVICE.md -o build/GETTING_STARTED_SSI_SERVICE.md
```

## Ideas 
_Brainstorm here._

## Open Questions

These are open for discussion as Issues:

* [CLI Tools and Scripting Requirements Discussion](https://github.com/TBD54566975/tbd-tutorials/issues/1)

## Analogy to Similar Systems

The Quarkus project runs a similar setup for tutorials, examples, and 
quickstarts called ["Guides"](https://quarkus.io/guides/).

Each guide has a docs page, kind of like a blog post which shows how 
to run it and what it’s about. For example, 
[this is the Getting Started doc](https://quarkus.io/guides/getting-started).

The sections in the docs are generally:

* How to get the example
* How to build it
* How to run it
* What concept it’s showing
* How to test it
* How to apply similar concepts in your code

All of the quickstarts live in 
[one repo](https://github.com/quarkusio/quarkus-quickstarts).

And because there’s a common way they’re built, they can be surfaced 
on the site and tested and run in a uniform way.
It’s a nice example because the end user facing thing is surfaced on the 
site, everything’s tested, and everything is backed by real code 
that’s protected against going stale (tests would fail, prompting 
maintenance and a check against docs to ensure they’re up to date).

## Project Information
_TODO_

Project leads should complete, alongside this `README`:
* [CODEOWNERS](./CODEOWNERS) - set project lead(s)
* [CONTRIBUTING.md](./CONTRIBUTING.md) - Fill out how to: install prereqs, build, test, run, access CI, chat, discuss, file issues

The other files in this template repo may be used as-is:
* [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md)
* [GOVERNANCE.md](./GOVERNANCE.md)
* [LICENSE](./LICENSE)

## Project Resources

| Resource                                   | Description                                                                    |
| ------------------------------------------ | ------------------------------------------------------------------------------ |
| [CODEOWNERS](./CODEOWNERS)                 | Outlines the project lead(s)                                                   |
| [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md) | Expected behavior for project contributors, promoting a welcoming environment |
| [CONTRIBUTING.md](./CONTRIBUTING.md)       | Developer guide to build, test, run, access CI, chat, discuss, file issues     |
| [GOVERNANCE.md](./GOVERNANCE.md)           | Project governance                                                             |
| [LICENSE](./LICENSE)                       | Apache License, Version 2.0                                                    |