---
title: Instructions for Getting Set Up for Bioinformatics Work
#date: 2024-01-01
type: page

# Optional
summary: "Instructions for Getting Set Up for Bioinformatics Work"
#image:
#  filename: featured.jpg
#  caption: "Photo by..."

# Draft mode (won't publish until set to false)
draft: false
---

The purpose of this page is to provide a set of instructions for getting you set up to run bioinformatics pipelines on our lab server (delltronXL) or ACENET's remote servers (e.g. fir, nibi, etc). Consider this a living document, and make any suggestions for changes and additions that you might find useful.

## Basic Setup

- Windows: Install WSL (Windows Subsystem for Linux)
- Mac: Make sure `ssh` is installed on your Terminal app
- Linux: As for Mac

## Bioinformatics Crash Course Resources

- [Practical Computing for Biologists](https://practicalcomputing.org/) is a great textbook to introduce you to the shell and programming in general, written in an accessible style and intended for non-computer science majors (i.e. all of us). It will make you "dangerous" on the shell very quickly (in a good way). We have 2 hard copies in the lab, and there's another one at the library. The website (linked above) has some files etc that are referred to in the textbook.
- [Happy Belly Bioinformatics](https://astrobiomike.github.io/) is written by Mike Lee, who I met at USC when I was a postdoc there. It's another really accessible intro to the shell and some other types of analyses like metagenomics and metabarcoding.

## Tips 'n' Tricks

- Make sure you know where you are. Learn the Linux file system structure and what `pwd` does.
- Set up aliases for `rm`, `cp`, `mv` in your config file (see more on this below) to avoid doing stupid stuff. All you need to do is add an `-i` flag for all 3, i.e. `alias rm='rm -i'`
- Run `ls` before doing any command like `cp`, `mv`, `rm` just to make sure you know what you're doing.
- Learn how to use `ls`, `vi`/`nano`, `chmod`, `grep`, `sed`, `less`, `cat`, `zcat`, `wc`. I use these tools all the time. Good use cases are counting the unumber of records in a .fasta or .fastq file, making scripts executable, etc.

## Getting Connected by SSH

1. Ask for an account to be created for you on `delltronXL`, the lab server.
2. *Optional (depends on whether your research needs it):* [Sign up for ACENET/CCDB](https://ccdb.alliancecan.ca/account_application), then let Jesse know **your username** so he can add you to the lab account. Once you've been approved, log in to your CCDB account, go to "Resources", "Access Systems", and ask for access to every server (HPC only) there. We may not use all of them, but good to just ask. Next, add MFA by going to "My Account" and then "Multifactor Authentication".
3. Check to see whether you can log in to the lab server by `ssh`, i.e.:
```
ssh username@delltronxl.ad.stfx.ca #this method may not work for students
OR
ssh username@141.109.38.34
```
4. Next, set up your `ssh` keys to allow password-free access according to the [instructions here](https://gist.github.com/stormpython/9517102).
5. Now, let's make login in to the server easier by adding a shortcut called an **alias** to your configuration file. If you're on Mac, your configuration file will probably be `~/.bash_profile`, and if you're on Linux/WSL, your configuration file will be `~/.bashrc`.
6. Let's use a simple command-line text editor called `vim` to edit this file. To edit your configuration file with vim, run:

```
vi ~/.bashrc

OR

vi ~/.bash_profile
```
7. Once you're in `vim`, there are a couple things to remember. There is **command mode** (you will start in this mode) and **insert mode**. To get into insert mode, just press the key "i". Command mode allows you to do all sorts of dangerous things like deleting the entire document with a couple keystrokes (i.e. "dG"). So, it's important to first learn how to get out of the file without making any changes. To do this, type (in the following order): escape key, ":", "q" (quit), "!" (get me out of here!). This should bring you back to your terminal. Practice this a couple of times (for fun, try the "dG" command or random keys on the keyboard).
8. Once you can safely get in and out of the file you're editing without making changes, now it's time to edit to add an alias. Follow the formatting of other aliases in your `.bashrc` to add one in, e.g. `alias dxl='ssh jessem@delltronxl.ad.stfx.ca'`.
9. Next, learn how to use `tmux` / `screen` to keep remote sessions alive on delltronXL.
10. Next, put your ssh keys up on all of the ACENET servers so you never need to use a password again.
11. If you are doing a bioinformatics-based project (or even have a component that is bioinformatics) I would like you to set up a github account and join [our github group](https://github.com/stfx-microeco-lab). That way, you can start sharing code with me and others in the group right away. If this applies to you, talk to me about the procedure to get this set up and we can write up a protocol together that will live on this site.
