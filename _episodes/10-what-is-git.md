---
title: "What is Git/GitHub?"
teaching: 10
exercises: 0
questions:
- "What is Git?"
- "What is Github?"
objectives:
- "explain why version control is useful"
- "explain the difference between Git and GitHub"
keypoints:
- "Git and Github are not the same"
- "You can use Git for version control"
- "You can use GitHub for collaboration and open sourcing your work!"
---

- Summary of content and terms
- Include links to more reference material

### What is Version Control

Version control is a name used for software which can help you record changes you make to the files in a directory on your computer. Version control software and tools (such as Git, SVN, and Mercurial) are often associated with software development. Increasingly, they can are being used for all kinds of files across research and academic collaborations. Version control systems work best with plain text files such as documents or computer code, but modern version control systems can be used to track changes in any type of file.

### What is Git and GitHub?

We often hear the terms **_Git_** and **_GitHub_** used interchangeably but they are completely different things.

**_Git_** is one of the most widely used version control systems in the world. It is a free, open source tool that can be downloaded to your local machine and used for logging all changes made to a group of designated files (referred to as a "git repository" or "repo" for short) over time. It can be used to control file versions locally by you alone on your computer, but is perhaps most powerful when employed to coordinate simultaneous work on a group of files shared among distributed groups of people.

Once installed, interaction with Git is done through the Command Prompt in Windows, or the Terminal on Mac/Linux. Since Word documents contain special formatting, Git unfortunately cannot version control those, nor can it version control PDFs, though both file types can be stored in Git repositories. Git can version any *plain text* file such as `.csv`, `.txt`, `.json`, and more. 

**_GitHub_** on the other hand is a popular website for hosting and sharing Git repositories remotely. It offers a web interface and provides functionality and a mixture of both free and paid services for working with such repositories. The majority of the content that GitHub hosts is open source software, though increasingly it is being used for other projects such as open access journals, blogs, and constantly updated text books. 

*What can understanding GitHub do for Librarians?*

* A place to discover and reuse ("fork") a huge amount of openly licensed digital projects and open source software
* A new and alternative means for publishing content online. Any GitHub repository can have its own project website, blog and wiki using GitHub Pages.

#### Why is Git important for librarians & archivists?
Rather than emailing documents with tracked changes and some comments and renaming different versions of files (example.txt, exampleV2.txt, exampleV3.text) to differentiate them, we can use *version control* to save (or in Git parlance, "commit") all that information with the document itself. This makes it easy to get an overview of all changes made to a file over time by looking at a log of all the changes that have been made. And all earlier versions of each file still remain in their original form: they are not overwritten, should we ever wish to "roll back" to them.

The few most important factors of version control are:

* **Collaboration** - Version control allows us to define formalized ways we can work together and share writing and code. For example merging together sets of changes from different parties enables co-creation of documents and software across distributed teams. When several people collaborate in the same project, it's possible to accidentally overlook or overwrite someone's changes. The version control system automatically notifies users whenever there's a conflict between one person's work and another's.
* **Versioning** - Having a robust and rigorous log of changes to a file, without renaming files (v1, v2, _final_copy_)
* **Rolling Back** - Version control allows us to quickly undo a set of changes. This can be useful when new writing or new additions to code introduce problems. Since all old versions of files are saved, it's always possible to go back in time to see exactly who wrote what on a particular day.
* **Understanding** - Version control can help you understand how the code or writing came to be, who wrote or contributed particular parts, and who you might ask to help understand it better. As we have this record of who made what changes when, we know who to ask if we have questions later on, and, if needed, revert to a previous version, much like the “undo” feature in an editor.
* **Backup** - While not meant to be a backup solution, using version control systems mean that your code and writing can be stored on multiple other computers. Nothing that is committed to version control is ever lost, unless you work really, really hard at it.
