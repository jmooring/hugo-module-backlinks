# Hugo Module &ndash; Backlinks

This Hugo module allows you to render a list of pages that link to the current page.

## Configuration

To add this module to your project, initialize your project as a Hugo module:

```sh
hugo mod init foo
```

In the above, `foo` is typically something like `github.com/user/project`.

Then add this to your site configuration:

```toml
[[module.imports]]
path = 'github.com/jmooring/hugo-module-backlinks'

[markup.goldmark.renderHooks.link]
enableDefault = true

[outputs]
home = ['html','rss','backlinks']
```

To override the list title, create a `backlinks_title` translation entry in your `i18n` files.

## Usage

To use the backlinks partial:

```text
{{ partial "backlinks.html" . }}
```

## Try it

```text
git clone --single-branch -b hugo-github-issue-8077 https://github.com/jmooring/hugo-testing hugo-github-issue-8077
cd hugo-github-issue-8077
hugo server
```
