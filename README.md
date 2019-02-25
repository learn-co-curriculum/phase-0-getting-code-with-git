# Getting Code with Git

## Learning Goals

- Identify a _remote_ repository
- Copy a repository to your local machine with `git clone`
- List remotes with `git remote`
- Duplicate other organizations' repositories into your own via GitHub with `git fork` 

## Introduction

Now that we've created local Git repositories, we can create logged histories of
our projects. What's great about Git and [open
source](https://opensource.com/resources/what-open-source) is that lots of
people are _doing the exact same thing_ all around the world all the time.

Our next step is to learn how to get others' repositories. In a later
lesson we'll cover how to push our locally-created repositories onto the
internet so that others can see our projects. But one step at a time.

## Identify a _remote_ Repository

To work with or collaborate on any Git project, you need to be able to manage
your _remote_ repositories. Remote repositories are versions of a repository
that are hosted online—typically, on GitHub.

## Copy a Repository to Your Local Machine with `git clone`

We use `git clone` to copy someone else's remote copy of their local repository
to our machine.

1. Navigate to the https://github.com/facebook/react repository
2. Click the "Clone or Download" green button on the right.
2. Make sure you select `Use SSH` as your URL type.

![SSH URL](https://files.readme.io/UgsI2ndmR2aH5ky5G1OA_GitHub%20-%20SSH%20-%201.png)

3. Click the "Copy to clipboard" button (highlighted below). This will copy the
URL for us to use when we clone.

![Clone Repo Button](http://readme-pics.s3.amazonaws.com/clone-repo-clone-url-button.png)

4. In the terminal (accessed through the 'Sandbox' or Learn IDE), we run the
`git clone` command. It takes the URL we just copied as an argument, like so:

```bash
git clone your-copied-github-url
```

This will create a local copy of the GitHub repository on our own machine.

## List Remotes with `git remote`

If you use the `ls` command, you'll see Git created a directory called
`react`. Use `cd` to enter that directory.

```bash
cd react
```

Type `git remote` to see each remote available.

If you've cloned your repository, you should at least see `origin`. The remote
called `origin` is the default name Git gives to the remote you cloned from:

```bash
$ git remote
origin
```

## Duplicate Other Organizations' Repositories into Your Own via GitHub with `git fork`

Forking a GitHub repository is just a way to create a personal, online duplicate
of it. When you fork a lab, GitHub creates a duplicate from the source
organization's online version of the repository to **your** local duplicate of
the repo.

It's like saying "Hey, can I have the Louvre's version of _The Mona Lisa_?" The
Louve would say no. If you were to create an exact online duplicate by _forking_
it from `louvre/mona_lisa` to `your-name/mona_lisa` the Louvre would be cut out
of the, pardon the pun, picture. You could then copy *your* organization's
version to *your* local machine with `git clone`.

![Fork Button](http://readme-pics.s3.amazonaws.com/fork_button.jpg)

Forking is a very common workflow for working with teams or working with or
contributing to open sourced content in the GitHub community.  You can fork any
repository by clicking the "Fork" button at the top right of any GitHub
repository.

Let's try a _fork_ and _clone_ workflow.

Click the GitHub icon at the top of this page:

![GitHub Octocat Icon](https://flatiron-client-assets.s3.amazonaws.com/assets/github-learn-button.png)

This will bring you to the "learn-co-students" version of this lesson. Click the
'Fork' button in the upper right corner of the page. You will be prompted to
choose where the repository should be forked to, so go ahead and choose your
account. GitHub will take a few moments to create the fork, then navigate to
your copy of the repository. If all has gone well, you will see your username at
the top of the page, followed by a `/` and the name of the repository, along
with a link just below to the original repository. ([More on forking in the GitHub docs](https://help.github.com/enterprise/2.2/user/articles/fork-a-repo/).)

The important take away is to **not** misuse "fork" and "clone" when speaking
with other Git users. To get a local copy: **clone**; to make an online copy of
a repository to your personal organization so that you have the ability to
update its `master` branch, **fork**.

> Often, the original authors will include license information regarding how you
> can use their repository, so make sure to check before you publish, sell or
> distribute any material you've forked, cloned and modified.

## Conclusion

GitHub gives developers many ways to collaborate. Using `git fork` and `git
clone` together allows you to make local copies of others' code. As you saw with
cloning React, this is something you can do on _any_ public GitHub repository.
So if you've found a GitHub repository that you'd love to modify for your own
use, you can use this process to make your own copy and modify away.
