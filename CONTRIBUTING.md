# Contributing Guidelines

We welcome contributions from the community and first want to thank you for taking the time to contribute to this project!

Please familiarize yourself with the [Code of Conduct](CODE_OF_CONDUCT.md) and [Developer Certificate of Origin](./Developer%20Certificate%20of%20Origin.md) before contributing. All contributions to this repository must be signed as described on that page. Your signature certifies that you wrote the patch or have the right to pass it on as an open-source patch. [^2]

Please read through this document before submitting any issues or pull requests to ensure we have all the necessary information to effectively respond to your bug report or contribution.

## Ways to contribute

We welcome many different types of contributions and not all of them need a Pull request. Contributions may include:

* New features and proposals
* Documentation
* Bug fixes
* Issue Triage
* Answering questions and giving feedback
* Helping to onboard new contributors
* Other related activities

## Reporting Bugs, Features, and Enhancements

We welcome you to use the GitHub issue tracker to report bugs or suggest features and enhancements.

When filing an issue, please check existing open, or recently closed, issues to make sure someone else hasn't already reported the issue.

Please try to include as much information as you can. Details like these are incredibly useful:

* A reproducible test case or series of steps.
* Any modifications you've made relevant to the bug.
* Anything unusual about your environment or deployment.

## Contributing

Contributions are welcome from anyone with a GitHub account. However only moderators of the individual repository can commit to a branch. This is in order to ensure the changes are aligned to an issue, to our standards and not create a breaking change.

This is a rough outline of what a contributor's workflow looks like:

* Open and issue in the repository
* Make a fork of the repository within your GitHub account
* Create a topic branch from where you want to base your work. [^1]
* Modify the source; please focus on the **specific** change you are contributing.
* Ensure local tests pass.
* Updated the documentation. [^1]
* Make commits of logical units.
* Commit to your fork [using a clear commit messages](#formatting-commit-messages) and signed. [^2]
* Push your changes to a topic branch in your fork of the repository. [^1]
* Create a pull request containing that commit and link to the issue

Contributions via pull requests are appreciated. Before sending us a pull request, please ensure that:

1. You open an issue and link your pull request to the issue for context.
1. You are working against the latest source on the `main` branch.
1. You check existing open, and recently merged, pull requests to make sure someone else hasn't already addressed the problem.

We follow the GitHub workflow and you can find more details on the [GitHub flow documentation](https://docs.github.com/en/get-started/quickstart/github-flow). GitHub provides additional document on [forking a repository](https://help.github.com/articles/fork-a-repo/) and [creating a pull request](https://help.github.com/articles/creating-a-pull-request/).

For example:

```shell
git remote add upstream https://github.com/tenthirtyam/container-terraform.git
git checkout -b my-new-feature main
git commit -s -a
git push origin my-new-feature
```

### Staying In Sync With Upstream

When your branch gets out of sync with the remote main branch, use the following to update:

```shell
git checkout my-new-feature
git fetch -a
git pull --rebase upstream main
git push --force-with-lease origin my-new-feature
```

### Updating Pull Requests

If your pull request fails to pass or needs changes based on code review, you'll most likely want to squash these changes into existing commits.

If your pull request contains a single commit or your changes are related to the most recent commit, you can simply amend the commit.

```shell
git add .
git commit -s --amend
git push --force-with-lease origin my-new-feature
```

If you need to squash changes into an earlier commit, you can use:

```shell
git add .
git commit -s --fixup <commit>
git rebase -i --autosquash main
git push --force-with-lease origin my-new-feature
```

Be sure to add a comment to the pull request indicating your new changes are ready to review, as GitHub does not generate a notification when you `git push`.

### Formatting Commit Messages

We follow the conventions on [How to Write a Git Commit Message](http://chris.beams.io/posts/git-commit/).

Be sure to include any related GitHub issue references in the commit message.

See [GFM syntax](https://guides.github.com/features/mastering-markdown/#GitHub-flavored-markdown) for referencing issues and commits.

### Configure git to Automatically Sign Commits

git can be configured to automatically sign each commit. This is achieved by simply adding your name and your email address to your git config file, such as:

```shell
git config --global user.name "FIRST_NAME LAST_NAME"
git config --global user.email "MY_NAME@example.com"
```

You can also add an alias to always sign off on commits so that tools such as Visual Studio Code will do it:

```shell
git config --global alias.c "commit -s"
```

## Reporting Bugs and Creating Issues

For specifics on what to include in your report, please follow the guidelines in the issue and pull request templates when available.

[^1]: May not be required
[^2]: All commits must be signed by adding Signed-off-by: Your Name <your@email.com> to the last line of each Git commit message. The e-mail address used to sign must match the e-mail address of the Git author. If you set your user.name and user.email git config values, you can sign your commit automatically with git commit -s