[bep]: https://github.com/spf13
[bugs]: https://github.com/gohugoio/hugo/issues?q=is%3Aopen+is%3Aissue+label%3ABug
[contributing]: CONTRIBUTING.md
[create a proposal]: https://github.com/gohugoio/hugo/issues/new?labels=Proposal%2C+NeedsTriage&template=feature_request.md
[documentation repository]: https://github.com/gohugoio/hugoDocs
[documentation]: https://gohugo.io/documentation
[dragonfly bsd, freebsd, netbsd, and openbsd]: https://gohugo.io/installation/bsd
[forum]: https://discourse.gohugo.io
[friends]: https://github.com/gohugoio/hugo/graphs/contributors
[go]: https://go.dev/
[hugo modules]: https://gohugo.io/hugo-modules/
[installation]: https://gohugo.io/installation
[issue queue]: https://github.com/gohugoio/hugo/issues
[linux]: https://gohugo.io/installation/linux
[macos]: https://gohugo.io/installation/macos
[prebuilt binary]: https://github.com/gohugoio/hugo/releases/latest
[requesting help]: https://discourse.gohugo.io/t/requesting-help/9132
[spf13]: https://github.com/spf13
[static site generator]: https://en.wikipedia.org/wiki/Static_site_generator
[support]: https://discourse.gohugo.io
[themes]: https://themes.gohugo.io/
[twitter]: https://twitter.com/gohugoio
[website]: https://gohugo.io
[windows]: https://gohugo.io/installation/windows

<a href="https://gohugo.io/"><img src="https://raw.githubusercontent.com/gohugoio/gohugoioTheme/master/static/images/hugo-logo-wide.svg?sanitize=true" alt="Hugo" width="565"></a>

A fast and flexible static site generator built with love by [bep], [spf13], and [friends] in [Go].

---

[![GoDoc](https://godoc.org/github.com/gohugoio/hugo?status.svg)](https://godoc.org/github.com/gohugoio/hugo)
[![Tests on Linux, MacOS and Windows](https://github.com/gohugoio/hugo/workflows/Test/badge.svg)](https://github.com/gohugoio/hugo/actions?query=workflow%3ATest)
[![Go Report Card](https://goreportcard.com/badge/github.com/gohugoio/hugo)](https://goreportcard.com/report/github.com/gohugoio/hugo)

[Website] | [Installation] | [Documentation] | [Support] | [Contributing] | [Twitter]

## Overview

Hugo is a [static site generator] written in [Go], optimized for speed and designed for flexibility. With its advanced templating system and fast asset pipelines, Hugo renders a complete site in seconds, often less.

Due to its flexible framework, multilingual support, and powerful taxonomy system, Hugo is widely used to create:

- Corporate, government, nonprofit, education, news, event, and project sites
- Documentation sites
- Image portfolios
- Landing pages
- Business, professional, and personal blogs
- Resumes and CVs

Use Hugo's embedded web server during development to instantly see changes to content, structure, behavior, and presentation. Then deploy the site to your host, or push changes to your Git provider for automated builds and deployment.

Hugo's fast asset pipelines include:

- CSS bundling &ndash; transpilation (Sass), tree shaking, minification, source maps, SRI hashing, and PostCSS integration
- JavaScript bundling &ndash; transpilation (TypeScript, JSX), tree shaking, minification, source maps, and SRI hashing
- Image processing &ndash; convert, resize, crop, rotate,  adjust colors, apply filters, overlay text and images, and extract EXIF data

And with [Hugo Modules], you can share content, assets, data, translations, themes, templates, and configuration with other projects via public or private Git repositories.

## Sponsors

<p>&nbsp;</p>
<p float="left">
  <a href="https://www.linode.com/?utm_campaign=hugosponsor&utm_medium=banner&utm_source=hugogithub" target="_blank"><img src="https://raw.githubusercontent.com/gohugoio/gohugoioTheme/master/assets/images/sponsors/linode-logo_standard_light_medium.png" width="200" alt="Linode"></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <a href="https://cloudcannon.com/hugo-cms/?utm_campaign=HugoSponsorship&utm_source=sponsor&utm_content=gohugo" target="_blank"><img src="https://raw.githubusercontent.com/gohugoio/gohugoioTheme/master/assets/images/sponsors/cloudcannon-blue.svg" width="220" alt="CloudCannon"></a>
<p>&nbsp;</p>

## Installation

Install Hugo from a [prebuilt binary], package manager, or package repository. Please see the installation instructions for your operating system:

- [macOS]
- [Linux]
- [Windows]
- [DragonFly BSD, FreeBSD, NetBSD, and OpenBSD]

## Build from source

Hugo is available in two editions: standard and extended. With the extended edition you can:

- Encode to the WebP format when processing images. You can decode WebP images with either edition.
- Transpile Sass to CSS using the embedded LibSass transpiler. The extended edition is not required to use the Dart Sass transpiler.

Prerequisites to build Hugo from source:

- Standard edition: Go 1.19 or later
- Extended edition: Go 1.19 or later, and GCC

Build the standard edition:

```text
go install github.com/gohugoio/hugo@latest
```

Build the extended edition:

```text
CGO_ENABLED=1 go install -tags extended github.com/gohugoio/hugo@latest
```

## Documentation

Hugo's [documentation] includes installation instructions, a quick start guide, conceptual explanations, reference information, and examples.

Please submit documentation issues and pull requests to the [documentation repository].

## Prerequisites 

```
1. install hugo //下载hugo编译文件
2. install git 
```



## Add Content

新增文章

```shell
hugo new posts/my-first-post.md
```

修改文章属性

```markdown
---
title: "My First Post"
categoried: 分类
date: 2022-11-20T09:03:20-08:00
tags:
	- 标签1
	- 标签2
draft: true
---
```



## Debug

```
hugo server -D	//启动服务 -D 生成草稿
```



## Publish

```
hugo -D		//生成草稿
git commit 	//git提交github.io
```



## Hugo Help

```shell
PS W:\www\nicko-ch.github.io> hugo help
hugo is the main command, used to build your Hugo site.

Hugo is a Fast and Flexible Static Site Generator
built with love by spf13 and friends in Go.

Complete documentation is available at http://gohugo.io/.

Usage:
  hugo [flags]
  hugo [command]

Available Commands:
  completion  generate the autocompletion script for the specified shell
  config      Print the site configuration
  convert     Convert your content to different formats
  deploy      Deploy your site to a Cloud provider.
  env         Print Hugo version and environment info
  gen         A collection of several useful generators.
  help        Help about any command
  import      Import your site from others.
  list        Listing out various types of content
  mod         Various Hugo Modules helpers.
  new         Create new content for your site
  server      A high performance webserver
  version     Print the version number of Hugo

Flags:
  -b, --baseURL string             hostname (and path) to the root, e.g. http://spf13.com/
  -D, --buildDrafts                include content marked as draft
  -E, --buildExpired               include expired content
  -F, --buildFuture                include content with publishdate in the future
      --cacheDir string            filesystem path to cache directory. Defaults: $TMPDIR/hugo_cache/
      --cleanDestinationDir        remove files from destination not found in static directories
      --config string              config file (default is path/config.yaml|json|toml)
      --configDir string           config dir (default "config")
  -c, --contentDir string          filesystem path to content directory
      --debug                      debug output
  -d, --destination string         filesystem path to write files to
      --disableKinds strings       disable different kind of pages (home, RSS etc.)
      --enableGitInfo              add Git revision, date and author info to the pages
  -e, --environment string         build environment
      --forceSyncStatic            copy all files when static is changed.
      --gc                         enable to run some cleanup tasks (remove unused cache files) after the build
  -h, --help                       help for hugo
      --i18n-warnings              print missing translations
      --ignoreCache                ignores the cache directory
      --ignoreVendor               ignores any _vendor directory
      --ignoreVendorPaths string   ignores any _vendor for module paths matching the given Glob pattern
  -l, --layoutDir string           filesystem path to layout directory
      --log                        enable Logging
      --logFile string             log File path (if set, logging enabled automatically)
      --minify                     minify any supported output format (HTML, XML etc.)
      --noChmod                    don't sync permission mode of files
      --noTimes                    don't sync modification time of files
      --path-warnings              print warnings on duplicate target paths etc.
      --poll string                set this to a poll interval, e.g --poll 700ms, to use a poll based approach to watch for file system changes
      --print-mem                  print memory usage to screen at intervals
      --quiet                      build in quiet mode
      --renderToMemory             render to memory (only useful for benchmark testing)
  -s, --source string              filesystem path to read files relative from
      --templateMetrics            display metrics about template executions
      --templateMetricsHints       calculate some improvement hints when combined with --templateMetrics
  -t, --theme strings              themes to use (located in /themes/THEMENAME/)
      --themesDir string           filesystem path to themes directory
      --trace file                 write trace to file (not useful in general)
  -v, --verbose                    verbose output
      --verboseLog                 verbose logging
  -w, --watch                      watch filesystem for changes and recreate as needed

Additional help topics:
  hugo check      Contains some verification checks

Use "hugo [command] --help" for more information about a command.
```

