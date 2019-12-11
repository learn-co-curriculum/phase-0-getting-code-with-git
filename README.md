# Getting Code with Git

## Learning Goals

- Copy a repository to your local machine with `git clone`
- List remotes with `git remote`
- Duplicate other organizations' repositories into your own via GitHub with the "Fork" button

## Introduction

Git repositories let us create logged histories of the versions of the files
we "track." Just think, right now, around the world people are using Git
to track their projects: Star Trek Fan Fiction, resumes, Ruby Code, JavaScript
code, PhD theses, etc.

Git not only lets you track files in a local repo on your machine, you can "share"
your repo on the internet so that others can use your code. In this lesson
we'll discuss how to get others' repositories.

In a later lesson we'll cover how to push _our_ locally-created repositories onto the
internet so that others can see our projects.

## Copy a Repository to Your Local Machine with `git clone`

We use `git clone` to copy someone else's repo from the internet to our _local_ machine.
We are not getting _their_ repo from _their_ local machine (that would be very creepy).

Instead, they must have
already "mirrored" their _local_ repository onto the internet. In Git-speak we'd say
they would have had to have created a _remote repository_: a copy of their local repository,
but on the internet. We'll be cloning that _remote repository_.

Let's get the code for the popular ReactJS framework.

1.  Navigate to the https://github.com/facebook/react repository.
2.  Click the green "Clone or download" button on the right.
3.  Make sure you select `Use SSH` as your URL type.

    ![SSH URL](https://files.readme.io/UgsI2ndmR2aH5ky5G1OA_GitHub%20-%20SSH%20-%201.png)

4.  Click the "Copy to clipboard" button (highlighted below). This will copy the
    URL for us to use when we clone.

        ![Clone Repo Button](https://readme-pics.s3.amazonaws.com/clone-repo-clone-url-button.png)

5.  In the terminal, run the `git clone` command. It takes the URL we just copied as an argument, like so:

```bash
$ git clone your-copied-github-url
```

This will create a _local_ copy of the GitHub repository on our own machine.

## List Remotes with `git remote`

If you use the `ls` command, you'll see Git created a directory called
`react`. Use `cd` to enter that directory.

```bash
$ cd react
```

Type `git remote` to see the names of each remote repository (or, "remote") available.

Since you cloned your repository, you should see a remote name called `origin`. The remote
name `origin` is the default name Git gives to the remote you cloned from:

```bash
$ git remote
origin
```

Let's prove that the `origin` name has some relationship to the address GitHub gave us.

```bash
$  git remote show origin
* remote origin
  Fetch URL: git@github.com:facebook/react.git
```

The "remote address" `git@github.com:facebook/react.git` assigned to the
"remote name" - `origin` - is the same thing you copied from the
GitHub web interface. This confirms that the _remote repository_ you
_cloned_ automatically set up a _remote name_ called `origin`.

## Duplicate Other Organizations' Repositories into Your Own via GitHub with the "Fork" Button

Forking a GitHub repository is just a way to create a personal, online duplicate
of it. When you fork a repository, GitHub creates a duplicate of that repository
under your control.

If my GitHub username were `octocat` and I "forked" `facebook/react`, GitHub would
copy the remote repository `facebook/react` and create it under my name as
`octocat/react`. It's making a copy of one _remote repository_ to a new _remote
repository_.

It's like saying "Hey, can I have the Louvre's version of _The Mona Lisa_?" The
Louvre would say, "No." If you were to create a perfect online duplicate by _forking_
it from `louvre/mona_lisa` to `your-name/mona_lisa`, and then were to clone
from _that_ remote repository, then the Louvre can keep their copy and you can
update your copy as you choose.

![Fork Button](http://readme-pics.s3.amazonaws.com/fork_button.jpg)

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

The important take away is to **not** misuse the words "fork" and "clone" when speaking
with other Git users. To get a local copy: **clone**; to make an online copy of
a repository to your personal organization so that you have the ability to
update its `master` branch, **fork**.

> Often, the original authors will include license information regarding how you
> can use their repository, so make sure to check before you publish, sell or
> distribute any material you've forked, cloned and modified.

## Conclusion

GitHub gives developers many ways to collaborate. Using GitHub's "Fork" button and `git clone` together allows you to make copies of others' code.
