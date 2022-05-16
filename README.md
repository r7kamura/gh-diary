# gh-diary

[GitHub CLI](https://github.com/cli/cli) extension to open today's issue.

## Install

```
gh extension install r7kamura/gh-diary
```

## Usage

```bash
# Open the text editor to write comment to today's issue.
gh diary comment --repo foo/bar

# Open today's issue in the web browser.
gh diary web --repo foo/bar
```

Suppose today is May 9 2022, this command works as follows:

1. Create an issue titled "2022-05-09" if it doesn't exists on foo/bar repo
2. Open the text editor or the web broser

If you are working on foo/bar repo directory, you can omit `--repo foo/bar` option:

```bash
gh diary comment
```

## Background

I created this extension to use GitHub Issues as my diary by using [r7kamura/gialog](https://github.com/r7kamura/gialog).

- https://r7kamura.github.io/diary/

To easily open today's issue from anywhere, I'm using `gh d` alias like this:

```console
$ gh alias set d "diary web --repo r7kamura/diary"
- Adding alias for d: diary web --repo r7kamura/diary
✓ Added alias.
$ gh d
Opening github.com/r7kamura/diary/issues/1 in your browser.
```
