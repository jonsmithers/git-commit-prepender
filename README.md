
# Installation

`cd` to the root of your repo and run these commands:

```
curl "https://raw.githubusercontent.com/jonsmithers/git-commit-prepender/dev/prepare-commit-msg?" > ./.git/hooks/prepare-commit-msg
chmod +x ./.git/hooks/prepare-commit-msg
```

# Configuration

You can customize the prefix to be anything you want. Here are some examples:

```
git config commit.prefix "ticket-%t: "
git config commit.prefix "#%t) "
git config commit.prefix "\n\nMY-PROJECT: %t"
```

In every example `%t` will be substituted with a number found the branch name.
If no number is found, then no prefix is inserted.
