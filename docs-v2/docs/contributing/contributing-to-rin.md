---
title: Contributing
sidebar_position: 2
---

# Contributing

We are glad that you're willing to contribute to this project. We are usually very lenient and relaxed with the submissions of PRs, and Issues reports. But there are some stuff that you need to know before contributing.

## Requirements

To get started, you'll need these things installed:

- Git
- Python 3.10.x
- Pipenv

## Installing Dependencies

All of the dependencies can be found within `Pipfile` and `Pipfile.lock`, and requires Pipenv in order to be installed.  Git can be found [here](https://git-scm.com/). Python can be also found at its website ([Python's Official Website](https://www.python.org/)). Pipenv can be found [here](https://pipenv.pypa.io/en/latest).

Your only option is via [Pipenv](https://pipenv.pypa.io/en/latest/)

`pipenv install`

If you haven't set up the Pipenv yet, run this in the root directory of the git repository: 

`pipenv --python 3.10`

## Pull Requests and Commits

You have 2 option: Fork the repo and make a pull request back into the main one, or commit to the branch directly. Option 2 is preferred.

## Formatting

This projects uses a ton of linters and formatters. The main formatters are Black, AutoPEP8, and Isort. And there are a lot of linters as well. Most of them are from Codefactor, Codacy, and Deepsource. You don't have to worry about them because they are set up as formatters on the CI/CD workflow. Meaning that once it is done, all the code is formatted already.

## Tips about the Formatters

If you send a commit that has changes to the code, the Formatters will start kicking in. These exist as a CI Workflow, so make sure to wait 2-3 mins before you make any single change to the code. If you decide to commit and change a part of the main cogs, it will start complaining about merge conflicts. The workflow only formats the Cogs folder.

## Issue and Feature Requests Reports

If there is an issue or a feature you want to be added, use the built-in GitHub issue tracker. Though a system like Jira could be used, it would be more efficient to just use the issue tracker that GitHub provides.

- If submitting a issue report, follow the template. Duplicates will not receive support
- If submitting a feature request, follow the template as well. As with issue reports, duplicate requests will not receive support

## Releasing Tags
In order to automate the release system, you have to make sure that in order to use it, the git commit message must be done correctly. Only use this if there is a new update that is ready to be released. These are pretty similar to [Angular's Commit Message Conventions](https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#-git-commit-guidelines). Here's a table that should help with explaining this:

| Type of Release, Update, or Patch | Example |
|              :--:                 | :--:    |
| Major Release                     | `Release: v3.0.0` |
| Minor Release                     | `Update: v3.1.0`|
| Patch Release                     | `Fix: Instagram API Cog removal` |


## Git Commit StyleGuides

- If updating any other files that aren't project files or not important (stuff like README.md, contributing.md, etc), add the [skip ci] label in the front
- With each new commit, the message should be more or less describing the changes. Please don't write useless commit messages...
- If releasing tags, have it in this style. `Release: [insert what changed here]`, `Update: [insert what changed here]`, and `Fix: [insert what changed here]`. Release is a major release. This means it bumps from 1.0 to 2.0. Minor means it bumps up the version from 1.4 to 1.4.1 for example. And fix just applies a patch, which would be 1.4.1 to 1.4.1.1.
