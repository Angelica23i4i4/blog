---
title: About the Git version control system

# Summary for listings and search engines
summary: This chapter is about getting started with Git. First, we'll learn the basics of version control systems, then we'll move on to how to run Git on your OS and finally set it up for work. At the end of the chapter, you will already know what Git is and why you should use it, and you will also have a system that is finally configured to work.

# Link this post with a project
projects: []

# Date published
date: '2020-12-13T00:00:00Z'

# Date updated
lastmod: '2024-03-12T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin
 

tags:
  - Academic
  

categories:
  - Demo
---


## About the Git version control system

   What is a "version control system" and why is it important? A version control system is a system that records changes to a file or set of files over time and allows you to revert to a specific version later. For file version control, this book will use software source code as an example, although in reality you can use version control for almost any type of file.

## Local version control systems

  Many people use copying files into a separate directory (maybe even a timestamped directory if they're smart enough) as a method of version control. This approach is very common due to its simplicity, but it is incredibly error prone. It can be easy to forget which directory you are in and accidentally change the wrong file or copy the wrong files that you intended.

 To solve this problem, programmers long ago developed local VCSs with a simple database that keeps a record of all changes to files, thereby maintaining revision control.

![Local version control](git1.png)

  One popular VCS was the RCS system, which is still distributed with many computers today. RCS stores sets of patches (differences between files) on disk in a special format, using which it can recreate the state of each file at a given point in time.

## Centralized version control systems

 The next major problem that people face is the need to interact with other developers. In order to deal with it, centralized version control systems (Centralized Version Control System, hereinafter CVCS) were developed. Systems such as CVS, Subversion, and Perforce use a single server that contains all versions of files, and a number of clients that retrieve files from this centralized repository. CVCS has been the standard for many years.
 
![Centralized version control](git2.png)

  This approach has many advantages, especially over local VCS. For example, all project developers know to a certain extent what each of them does. Administrators have full control over who can do what, and it is much easier to administer CVCS than to operate local databases on each client.

  Despite this, this approach also has serious disadvantages. The most obvious disadvantage is the single point of failure represented by a centralized server. If this server goes down for an hour, then during that time no one will be able to use version control to save the changes they are working on, and no one will be able to share those changes with other developers.
 
## Distributed version control systems

   This is where distributed version control systems (DVCS) come into play. In a DVCS (such as Git, Mercurial, Bazaar or Darcs), clients don't just download a snapshot of all files (the state of the files at a certain point in time) — they copy the entire repository. In this case, if one of the servers through which the developers were communicating dies, any client repository can be copied to another server to continue working. Each copy of the repository is a complete backup of all data.
   
![Distributed version control](git3.png)

  Moreover, many DVCS can interact with multiple remote repositories at the same time, so you can work with different groups of people using different approaches at the same time within the same project. This allows you to use several development approaches at once, for example, hierarchical models, which is completely impossible in centralized systems.
