---
title: "Using git Locally and Syncing Changes"
teaching: 30
exercises: 20
questions:
- "What is a local and a remote repository?"
- "How do I get a local copy of a GitHub repository?"
- "How do I keep local and remote repositories synced up?"
objectives:
- "Clone a repository on GitHub"
- "Make changes locally to repository"
- "Use push to sync up local changes to GitHub"
- "Pull changes back from GitHub to the local repository"
keypoints:
- "`pull` is a Git verb for bringing changes from a remote repository to the local repository"
- "Git uses a two-stage commit process. Changes must first be added to the staging area, then committed from there"

---

- Clone the website GitHub repository they’ve been working on
- Make change and commit, push commit
- Make change and commit on remote repository, then pull? 

### Using Git

One of the main barriers to getting started with git is the language. Although some of the language used in git is 
fairly self-explanatory, other terms are not so clear. The best way to get to learn the language - which consists of a 
number of verbs such as `add`, `commit` and `push` (precdeded by the word 'git') - is by using it, which is what we will be doing during this 
lesson. These commands will be explained as we proceed from setting up a new version-controlled project to publishing 
our own website.

We will try to do this session as a group, but those who prefer to go at a slower pace can follow the instructions on 
the [GitHub page](https://github.com/data-lessons/library-git).

## Cloning a repository from GitHub

When we have logged in to GitHub, we can create a new repository by clicking the **+** icon in the upper-right corner of
any page then selecting **New repository**. Let's do this now.

* Create a new repository
* Give it the name `hello-world`

GitHub will ask if you want to add a README.md, license or a `.gitignore` file. Do not do any of that for now.

> ## Choosing a license
> Choosing a license is an important part of openly sharing your creative work online. For help in wading through the
> many types of open source licenses, please visit <https://choosealicense.com/>.
{: .callout}

### Displaying the current project's status

We can run the `git status` command to display the current state of a project. Let's do that now.

~~~
$ git status
~~~
{: .bash}
~~~
On branch master
Initial commit
nothing to commit (create/copy files and use "git add" to track)
~~~
{: .output}

The output tells us that we are on the master branch (more on this later) and that we have nothing to commit (no 
unsaved changes).


### Adding and committing

We'll now create and save our first project file. This is a two-stage process. First, we **add** any files for which 
we want to save the changes to a staging area, then we **commit** those changes to the repository. This two-stage 
process gives us fine-grained control over what should and should not be included in a particular commit.

Let's create a new file using the `touch` command, which is a quick way to create an empty file.

~~~
$ touch index.md
~~~
{: .bash}

The `.md` extension above signifies that we have chosen to format that we have 
chosen to use Markdown, a lightweight markup language with plain text formatting syntax. We will explore Markdown a 
bit later.

Let's check the status of our project again.

~~~
$ git status
~~~
{: .bash}
~~~
On branch master
Initial commit
Untracked files:
  (use "git add <file>..." to include in what will be committed)

    index.md

nothing added to commit but untracked files present (use "git add" to track)
~~~
{: .output}

This status is telling us that git has noticed a new file in our directory that we are not yet tracking. With colourised 
output, the filename will appear in red. To change this, and to tell Git we want to track any changes we make to 
index.md, we use `git add`.

~~~
$ git add index.md
~~~
{: .bash}

This adds our Markdown file to the **staging area** (the area where git checks for file changes). To confirm this we 
might want to use `git status` again.

~~~
$ git status
~~~
{: .bash}
~~~
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

    new file:   index.md
~~~
{: .output}

If we are using colourised output, we will see that the filename has changed colour (from red to green). Git also tells us that there
is a new file to be committed but, before we do that, let's add some text to the file.

We will open the file `index.md` with any text editor we have at hand (e.g. Notepad on Windows or TextEdit on Mac OSX) and enter `# Hello, world!`. The
hash character is one way of writing a header with Markdown. Now, let's save the file within the text editor and check if Git
has spotted the changes.

~~~
$ git status
~~~
{: .bash}
~~~
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   index.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   index.md
~~~
{: .output}

This lets us know that git has indeed spotted the changes to our file, but that it hasn't yet staged them, so let's add 
the new version of the file to the staging area.

~~~
$ git add index.md
~~~
{: .bash}

Now we are ready to  **commit** our first changes. 
Commit is similar to 'saving' a file to Git. 
However, compared to saving, a commit provides a lot more information about the changes we have made,
and this information will remain visible to us later.


~~~
$ git commit -m 'Add index.md'
~~~
{: .bash}
~~~
[master (root-commit) e9e8fd3] Add index.md
 1 file changed, 1 insertion(+)
 create mode 100644 index.md
~~~
{: .output}

We can see that one file has changed and that we made one insertion, which was a line with the text '#Hello, world!'. 
We can
also see the commit message 'Add index.md', which we added by adding the `-m` flag to `git commit`.
The commit message is used to record a short, descriptive, and specific summary of what we did to help us remember later on without having to look at the actual changes.
If we just run `git commit` without the `-m` option, Git will launch nano (or whatever other editor we configured as `core.editor`)
so that we can write a longer message.

Having made a commit, we now have a permanent record of what was changed, along with metadata about who made the commit and at what time.

> ## Staging Area
>
> If you think of Git as taking snapshots of changes over the life of a project,
> `git add` specifies *what* will go in a snapshot
> (putting things in the staging area),
> and `git commit` then *actually takes* the snapshot, and
> makes a permanent record of it (as a commit).
> If you don't have anything staged when you type `git commit`,
> Git will prompt you to use `git commit -a` or `git commit --all`,
> which is kind of like gathering *everyone* for the picture!
> However, it's almost always better to
> explicitly add things to the staging area, because you might
> commit changes you forgot you made. (Going back to snapshots,
> you might get the extra with incomplete makeup walking on
> the stage for the snapshot because you used `-a`!)
> Try to stage things manually,
> or you might find yourself searching for "git undo commit" more
> than you would like!
{: .callout}

But at the moment our changes are only recorded locally, on our computer. If we wanted to work collaboratively with someone else they would have no way of seeing what we've done.
