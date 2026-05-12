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
