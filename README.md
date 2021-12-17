# Getting Code with Git

## Learning Goals

- Copy a repository to your local machine with `git clone`
- List remotes with `git remote`
- Duplicate other organizations' repositories into your own via GitHub with the
  "Fork" button

## Introduction

In the previous lesson, we learned how Git allows us to create logged histories
of all the versions of the files we "track." Another great benefit of using Git
is that it makes it easy for developers to "share" code by "pushing" a copy of
their repo to the internet (specifically, to GitHub). From there, other
developers can **clone** down the code onto their own machine and use it.

Of course, you've been taking advantage of this feature of Git for a while with
the labs you've been working on in this course! For this reason, a lot of the
content in this lesson will be review.

The important thing to understand is that the forking and cloning workflow that
you've been using with labs can be used with _any_ repo available on GitHub. But
of course the learn-co gem is currently handling some of the steps for you, so
in this lesson, you'll learn how to accomplish those steps "by hand."

## Copy a Repository to Your Local Machine with `git clone`

Let's review the cloning process using a repo that _isn't_ part of the
curriculum. We can get the code for the popular ReactJS framework:

1) Navigate to the [React repository](https://github.com/facebook/react).

2) Click the green "Code" button on the right.

3) Make sure `SSH` is selected.

4) Click the copy button.

![clone-repo](https://curriculum-content.s3.amazonaws.com/phase-0/completing-assignments/clone-repo.gif)

5) In the terminal, navigate to where you want to put the repo. Type `git clone`
   and a space, then paste in the copied SSH link from GitHub. It should look
   like this:

```console
$ git clone git@github.com:facebook/react.git
```

This will create a _local_ copy of the GitHub repository on your machine.

## List Remote Repos with `git remote`

If you use the `ls` command, you'll see Git created a directory called `react`.
Use `cd` to enter that directory.

```console
$ cd react
```

The `git remote` command will return the names of each remote repository (or,
"remote") available. Go ahead and run the command; you should see a remote
named `origin` returned. This is the "nickname" that Git assigns by default to
whatever remote you cloned from:

```console
$ git remote
origin
```

To prove that the `origin` name points to the repo we cloned from GitHub, we can
run `git remote -v` (the `v` flag stands for "verbose"). You should see
something like this:

```console
$  git remote -v
origin	git@github.com:facebook/react.git (fetch)
origin	git@github.com:facebook/react.git (push)
```

Here you can see that the "remote address" (`git@github.com:facebook/react.git`)
assigned to the "remote name" (`origin`) is the same thing you copied from the
GitHub web interface. This confirms that the _remote repository_ you _cloned_
automatically set up a _remote name_ called `origin`.

In the next lesson we'll learn how to **push** code up to GitHub. The `git
remote` command is what will enable you to ensure that the code is being pushed
to the right place.

## Duplicate Other Organizations' Repositories into Your Own via GitHub with the "Fork" Button

This is also part of the workflow you've been using for labs: you create your
own personal copy of the lab by clicking the "Fork" button on Canvas. But you
can also fork a repo directly from its page on GitHub.

Let's go back to the [React repository](https://github.com/facebook/react) on
GitHub. In the upper right corner of the page, you'll see three buttons,
including a Fork button:

![Fork Button](http://readme-pics.s3.amazonaws.com/fork_button.jpg)

Clicking the Fork button on the page for this repo (or any other repo available
on GitHub) will make a copy of the repo and store it in _your_ GitHub account,
just the same as when you click the Fork button on a lab's Canvas page. Having
your own copy gives you the ability to update its `main` (or `master`) branch
without affecting the original repo.

> **Note**: You _could_ use this workflow for labs. Instead of clicking the Fork
> button on Canvas, you could click the **Octocat** icon next to it. That would
> open up the lab's repo _without_ forking it, and you could then fork the lab
> using the Fork button on the repo page.

> **However**, doing so would bypass the `learn-co` gem which means you will
> need to submit the lab by hand in Canvas and it will not be graded
> automatically. So be sure to continue using the Fork button on the Canvas page
> for labs!

## Conclusion

GitHub gives developers many ways to collaborate. Using GitHub's "Fork" button
and `git clone` together allows you to make copies of others' code.

Often, the original authors will include license information regarding how you
can use their repository, so make sure to check before you publish, sell or
distribute any material you've forked, cloned and modified.
