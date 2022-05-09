# gh-diary

[GitHub CLI](https://github.com/cli/cli) extension to open issue titled YYYY-MM-DD.

## Install

```
gh extension install r7kamura/gh-diary
```

## Usage

```bash
gh diary --repo foo/bar
```

Suppose today is May 9 2022, this command works as follows:

1. Create an issue titled "2022-05-09" if it doesn't exists on foo/bar repo
2. Open the issue in your web browser

If you are working on foo/bar repo directory, you can omit `--repo foo/bar` option:

```bash
gh diary
```

## Background

I created this extension to use GitHub Issues as my diary by using [r7kamura/gialog](https://github.com/r7kamura/gialog).

- https://r7kamura.github.io/diary/

To eaily open today's issue from anywhere, I'm using `gh d` alias like this:

```console
$ gh alias set d "diary --repo foo/bar"
- Adding alias for d: diary --repo foo/bar
✓ Added alias.
/home/r7kamura/ghq/github.com/r7kamura/gh-diary main
$ gh d
Opening github.com/foo/bar/issues/1 in your browser.
```
