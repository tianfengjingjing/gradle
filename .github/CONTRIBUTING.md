# Contributing to Gradle
Thank you for considering making a contribution to Gradle! This guide explains how to setup your environment for Gradle development, how to identify tasks to work on, and where to get help if you encounter trouble.

## Development Setup
In order to make changes to Gradle, you'll need:

* A text editor or IDE. We use and recommend [IntelliJ IDEA](http://www.jetbrains.com/idea/).
* A [Java Development Kit](http://www.oracle.com/technetwork/java/javase/downloads/index.html) (JDK) version 1.7 or higher
* [git](https://git-scm.com/) and a [GitHub account](https://github.com/join)

Gradle uses a pull request model for contributions. Fork [gradle/gradle](https://github.com/gradle/gradle) and clone your fork.

You can generate the IntelliJ project by running `./gradlew idea` (or `./gradlew.bat idea` for Windows), then "Open" it with IntelliJ.

## Choosing Tasks
If you'd like to contribute to Gradle but aren't sure where, please look for issues [labelled help-wanted](https://github.com/gradle/gradle/labels/help-wanted). We have designated these issues as good candidates for easy contribution.

## Making Changes

### Larger Changes (features or enhancements)
Before starting to work on a feature or a fix, it's generally a good idea to open a discussion about your proposed changes on the [Gradle Developer List](https://groups.google.com/forum/#!forum/gradle-dev).
Doing so helps to ensure that:
* You understand how your proposed changes fit with the strategic goals of the Gradle project.
* You can get early feedback on your proposed changes, and suggestions as to the best approach to implementation.
* We can all collaborate in creating a [design document](design-docs). This is _required_ for all changes that affect behavior or public API.
    
### Code Changes
All code contributions should contain the following:

* Unit Tests (we love Spock) for any logic introduced.
* Integration Test coverage of the bug/feature at the level of build execution.
* Documentation coverage in the user guide, DSL Reference and JavaDocs where appropriate.
* Javadoc `@author` tags and committer names are not used in the codebase (contributions are recognised in the commit history and release notes)

If you're not sure where to start, ask on the developer list. There's likely a number of existing examples to help get you going.

Try to ensure that your code & tests will run successfully on Java 6, and on both *nix and Windows platforms.
The [Gradle CI](http://builds.gradle.org/) will verify this, but it helps if things work first time.

* Avoid using features introduced in Java 1.7 or later
* Be careful to normalise file paths in tests. The `org.gradle.util.TextUtil` class has some useful utility functions for this purpose.

### Getting Help
If you run into any trouble, please reach out to us on the [help/discuss forum](https://discuss.gradle.org/c/help-discuss) or [tweet @Gradle](https://twitter.com/gradle).

### Creating Commits And Writing Commit Messages
The commit messages that accompany your code changes are an important piece of documentation, and help make your contribution easier to review.
Please consider reading [Wow to Write a Git Commit Message](http://chris.beams.io/posts/git-commit/). Minimally, follow these guidelines when creating public commits and writing commit messages.

* Keep commits discrete: avoid including multiple unrelated changes in a single commit.
* Keep commits self-contained: avoid spreading a single change across multiple commits. A single commit should make sense in isolation.
* The first line of your commit message should be a summary of the changes and intent of the change. Details should follow on subsequent lines, each line prefixed by '-'.
* If your commit pertains to a GitHub issue, include the issue number (e.g. #123) in the commit message.

### Pre-Push Check
It is not necessary to run _all_ checks before submitting a pull request, but we do recommend running `./gradlew :<subproject>:check` where `<subproject>` is the name of the sub-project that has changed. For example: `./gradlew :launcher:check`.

### Submitting Your Change
Before we can accept any code contributions, you must complete and electronically sign a [Gradle CLA](http://gradle.org/contributor-license-agreement/).

All code contributions should be submitted via a [pull request](https://help.github.com/articles/using-pull-requests) from a [forked GitHub repository](https://help.github.com/articles/fork-a-repo).

Once received, the pull request will be reviewed by a Gradle core developer. Your pull request will be given higher priority if you:
* Have first discussed the change on the Gradle Developer list.
* Have followed all of the Contribution Guidelines here.

After review, and usually after a number of iterations of development, your pull request may be merged into the Gradle distribution.

## Our Thanks
We deeply appreciate your effort toward improving Gradle. For any contribution, large or small, you will be immortalized in the release notes for the version you've contributed to. 
  
If you enjoyed this process, perhaps you should consider getting [paid to develop Gradle](https://gradle.org/gradle-jobs/)? 




