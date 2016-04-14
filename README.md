# repo

Repo is a tool built on top of Git.  Repo helps manage many Git repositories,
does the uploads to revision control systems, and automates parts of the
development workflow.  Repo is not meant to replace Git, only to make it
easier to work with Git.  The repo command is an executable Python script
that you can put anywhere in your path.

* Homepage: https://code.google.com/p/git-repo/
* Bug reports: https://code.google.com/p/git-repo/issues/
* Source: https://code.google.com/p/git-repo/
* Overview: https://source.android.com/source/developing.html
* Docs: https://source.android.com/source/using-repo.html
* [Submitting patches](./SUBMITTING_PATCHES.md)
=======
# Git-repo

A fork of git-repo from google https://gerrit.googlesource.com/git-repo. added some feature. 

## review path attribute

Originally `repo upload` push changes to `<user>@<host>:<port>/<project-name>`. But in my case, A directory to manage project is needed, and I don't wan't every project name contain that directory name. so I added a attr `path` to `remote` just like `fetch`.

then the url used by `repo upload` changed to `<user>@<host>:<port>/<path>/<project-name>` 


in manifest.xml:

```
<remote name="xyz"
  review="http://review.abc.xyz/"
  fetch="QCOM"
  path="QCOM" />
```
