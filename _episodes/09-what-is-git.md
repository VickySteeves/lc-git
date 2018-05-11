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

### Uses in a Library Context

Teams are not the only ones to benefit from version control: lone librarians can benefit immensely. Version control is much like provenance - you know which changes came from who, and when. Future you will be pleased there's a record of events to come back too. There are many examples of information professionals using git in their everyday work to make sure they have a record of changes. Consider these common library world scenarios!

#### Scenario 1: Local librarian looking to start a crowdsourcing project

A local librarian is looking to put thousands of historical photographs of the area online so that the community can help identify the people and places they depict. She combs the web for examples of existing crowdsourcing projects, and even though they all appear unique to each institution, she notices quite a few seem to have almost the exact same functionality and structure. Rather than build a whole new version from scratch herself, she wishes there was a way to just copy the code of an existing one, and modify it to reflect her project. She notices the GitHub icon at the bottom of one of the projects she likes, but clicking on the link just brings her to a confusing directory of files and oddly labeled buttons such as "Fork".  

> GitHub hosts open-licensed projects ... and allows any user to fork any public project. By clicking the "fork" button, any GitHub user can almost instantaneously create their own version of an existing project. That "forked" project can be used as the basis for a new project, or can be used to work out new features that can be merged back into the original. (From: [GitHub for Academics](http://www.digitalpedagogylab.com/hybridped/push-pull-fork-github-for-academics/) )

#### Scenario 2: Multiple librarians editing metadata for a collection

A librarian has exported a spreadsheet of metadata from a repository for cleaning and editing. She's working with a group of librarians and students, so they need to make sure edits don't conflict. They also need to be able to undo any edits and preserve the original metadata. Once edits are complete, the whole group wants to review the changes before re-ingesting the spreadsheet of metadata into the repository.

The team can choose to use Git by itself to track changes and resolve conflicts or they can choose to use GitHub to host the project so that users can collaborate and review changes on the Web. Git will preserve the original metadata as well as all edits. GitHub will facilitate discussion about what changes should be made, who should make them, and why.

> A great example of this is in the geoblacklight community. You can browse the GitHub organization, click on a repository (which corresponds to an institution) and view their metadata and its' change over time: [github.com/OpenGeoMetadata](https://github.com/OpenGeoMetadata).

#### Scenario 3: GitHub, small teams, and DAMs
You manage a small library that used GitHub to clone certain aspects of your digital asset management system using a larger library's system. However, a few months later, you realized there were certain glitches that you wanted to address. Using git will allow you to trace back to what went wrong and when (since all edits are recorded). Since git keeps all changes, you can also trace the initial creator of the digital asset management system that you created and reach out to them for feedback.