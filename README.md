
# Tips & Tricks: Git/GitHub Workflow
<font size="1">Tyler Boyd-Meredith | Monday, Feb 6th, 2023
</font>

## Outline
At this meeting, I will present the basics of the Git version control system that allows you to create recoverable snapshots of your code as you are developing it.

## Setup
Before we meet, make sure you can use Git from the Unix command line on your computer. You can check this by running the command ```git --version``` at the command line.

If you're using Windows, you should be able to follow along using the [Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/install) (though, I've never tried to use this command line interface).

Also, it's helpful to have the [`Protocols`](https://github.com/Brody-Lab/Protocols) repository on your computer. You can get the repository on your machine by running

```
$ git clone https://github.com/Brody-Lab/Protocols
```

This will make a folder called Protocols in the current working directory and dump the contents of the entire repository there.

You should also be a member of the Brody lab GitHub!

You could also configure your command prompt to show which branch you're in.

## Example project

```
$ mkdir example_project
$ cd example_project
$ git init
$ ls -lah
```

## Workflows
- single-branch
    - this is more or less how [Protocols](https://github.com/Brody-Lab/Protocols) is managed
- git-flow
    - this is more or less how [Brian's PulseInputDDM code](https://github.com/Brody-Lab/PulseInputDDM) is managed
- [GitHub Flow](#github-flow)
    - this is what I use

## GitHub Flow
- Anything on master branch is deployable
- All work happens on branches off of master
    - they should have descriptive names!
- Push to named branches whenever
    - Run `git fetch` to see what people are working
- Open [Pull Request](#pull-requests) to change master
    - comments (on individual lines!)
    - tagging people
    - automatic testing
- Merge after PR review
- Deploy after review

## Forking
- Used for open source work. Fork a project, work on it, and then open a [PR](#pull-requests) to get your changes into the main project.

## Pull Requests
- A great chance for code review!
- tag people for comments

## Unit testing and GitHub Actions

# Resources
- [GitHub-Flow](https://githubflow.github.io/)
- [git-flow](https://nvie.com/posts/a-successful-git-branching-model/)

---
