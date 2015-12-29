# Github Local Sync

A set of scripts for managing your local github repos.  They make the assumption that anything you've starred, you'll want to have locally cloned.  

### download-stars

    Usage: download-stars <OAUTH KEY>
    Example: download-stars 1234abcd

Downloads the `starred.json` file from github.

Requires your [personal access token](https://github.com/settings/tokens/new), which should be given **user**, and possibly **repo** rights.  I donno.

**Bug:** Only grabs the first 100 stars. Need to add support for pagination.

### missing

    Usage: missing <DIRECTORY>
    Example: missing /Users/tsaleh/code

Examines the git repositories in `DIRECTORY` and outputs all which _aren't_ starred on github.

Assumes that the repositories in `DIRECTORY` mimic the github `org/repo` pattern, as follows:

    ~/DIRECTORY $ ls -d */*
    daneden/animate.css
    discourse/discourse
    golangcookbook/golangcookbook.github.io
    jnunemaker/nunes
    ...

### browse-missing

    Usage: browse-missing <DIRECTORY>
    Example: browse-missing /Users/tsaleh/code

Examines the git repositories in `DIRECTORY` and opens all which _aren't_ starred in your browser, so you can star them or ignore them as you see fit.

Assumes that the repositories in `DIRECTORY` mimic the github `org/repo` pattern, as follows:

    ~/DIRECTORY $ ls -d */*
    daneden/animate.css
    discourse/discourse
    golangcookbook/golangcookbook.github.io
    jnunemaker/nunes
    ...

### sync-stars

    Usage: sync-stars <DIRECTORY>
    Example: sync-stars /Users/tsaleh/code

Clones or updates your starred repos on github to directories under `DIRECTORY`.

Assumes that the repositories in `DIRECTORY` mimic the github `org/repo` pattern, as follows:

    ~/DIRECTORY $ ls -d */*
    daneden/animate.css
    discourse/discourse
    golangcookbook/golangcookbook.github.io
    jnunemaker/nunes
    ...

