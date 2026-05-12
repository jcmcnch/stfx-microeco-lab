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

## Background Reading and Skills

- pcfb
- HBB

## Getting Connected by SSH

1. Ask for an account to be created for you on `delltronXL`, the lab server.
2. *Optional (depends on whether your research needs it):* [Sign up for ACENET](https://ccdb.alliancecan.ca/account_application), then let Jesse know **your username** so he can add you to the lab account.
3. Check to see whether you can log in to the lab server by `ssh`, i.e.:
```
ssh username@delltronxl.ad.stfx.ca #this method may not work for students
OR
ssh username@141.109.38.34
```
4. Next, set up your `ssh` keys to allow password-free access according to the [instructions here](https://gist.github.com/stormpython/9517102).
5. Now, let's make loggin in to the server easier by adding a shortcut called an **alias** to your configuration file. If you're on Mac, your configuration file will probably be `~/.bash_profile`, and if you're on Linux/WSL, your configuration file will be `~/.bashrc`.
6. Let's use a simple command-line text editor called `vim` to edit this file. To edit your configuration file with vim, run:

```
vi ~/.bashrc

OR

vi ~/.bash_profile
```
7. Once you're in `vim`, there are a couple things to remember. There is **command mode** (you will start in this mode) and **insert mode**. To get into insert mode, just press the key "i". Command mode allows you to do all sorts of dangerous things like deleting the entire document with a couple keystrokes (i.e. "dG"). So, it's important to first learn how to get out of the file without making any changes. To do this, type (in the following order): escape key, ":", "q" (quit), "!" (get me out of here!). This should bring you back to your terminal. Practice this a couple of times (for fun, try the "dG" command or random keys on the keyboard).
8. Once you can safely get in and out of the file you're editing, now it's time to edit. Add alias locally for login.
9. tmux / screen on DXL
10. ACENET access ssh keys
11. Github access
