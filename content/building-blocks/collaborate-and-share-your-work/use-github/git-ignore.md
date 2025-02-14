---
title: "Exclude Files From Versioning"
description: "Not all files should be tracked (e.g., datasets, or sensitive information). Learn how to exclude them from versioning!"
keywords: "git, github, versioning, gitignore, remove, sensitive"
#weight: 1
#date: 2020-11-11T22:01:14+05:30
draft: false
aliases:
  - /learn/gitignore
  - /use/gitignore
---

## Let Git/GitHub know which files to exclude from versioning

By default, Git/GitHub track *any* files that you have created, for example:
- large data files (that you wont be able to upload to GitHub),
- files that are generated by code (and hence need not to be versioned), and
- even sensitive passwords that you may have stored in your code accidentally.

Luckily, Git offers a convenient way to __exclude files and directories from versioning__.

1. Create a new file in your project's root directory, and call it `.gitignore` (remember to use the `.`!)

2. Edit the `.gitignore` file, and define which files or directories to exclude. For example, `**/DIRNAME` excludes any directory called `DIRNAME`, and `*pdf` excludes any PDF files.

3. Save the `.gitignore` file, and run `git status` in your repository - the excluded files and directories won't show up anymore!

## Example

Check out a few example `.gitignore` files for [inspiration](https://github.com/rgreminger/example-make-workflow/blob/master/.gitignore), or copy-paste the following to your own `.gitignore`:

{{% codeblock %}}
```txt
**/rbin/
**/raw/
*RData
*pdf
**/audit
**/input
**/output
**/temp
**/zip
*csv
*xlsx
*~*
*log
*.Rhistory
**/exports
**.ipynb_checkpoints
**__pycache__
*.log
slides/*.gz
slides/*.snm
slides/*.toc
slides/*.nav
slides/*.out
slides/*.aux
.RProfile
```
{{% /codeblock %}}
