---
date: 2016-02-19T17:08:05+08:00
description: hello
keywords:
- world
title: about
toc: "off"
---

Slender-Next
=======

Yet another sample theme for [Hugo](http://gohugo.io/) with [base16](https://github.com/chriskempson/base16) color schemes.
Based on [slender](https://github.com/CrimsonRay/slender), inspired by [hexo-theme-next](https://github.com/iissnan/hexo-theme-next)

### Screenshot

![screenshot](images/screenshot.png)

### Features

* Responsive
* Pagination
* [base16](https://github.com/chriskempson/base16) color schemes
* Code/syntax highlighting with [highlight.js 9.0.0](https://highlightjs.org/)
* Proper meta tags for SEO
* Optimized for Chinese User
* Google Analytics And Baidu Tongji integration
* Diqus And Duoshuo integration
* MathJax Support
* Table of Content
* Tags + Archive

### Color Schemes

![slender-color-schemes](images/slender-color-schemes.png)

### Installation

1. Make a new Hugo site

    ```none
    $ hugo new site your_site/
    ```

2. Install Slender

    ```none
    $ cd your_site/
    $ mkdir themes
    $ cd themes
    $ git clone https://github.com/overvenus/slender-next
    ```

### Configuration

```toml
# config.toml
# https://github.com/overvenus/slender-next

baseurl = "http://url-to-your-site.com/"
title = "Your Title"
# set "zh-Hans", turn on optimization.
languageCode = "en-US"
MetaDataFormat = "yaml"
theme = "slender-next"
paginate = 5
PaginatePath = "/page/"

[author]
    name = "Your Name"

[permalinks]

    # Permalink format for pages.
    page = "/:title/"

    # Permalink format for blog posts.
    post = "/:year/:month/:day/:title/"

[taxonomies]
    # tags -> menu.main.tags
    tag = "tags"
    # archive -> menu.main.archive
    archive = "archive"

[params]

    # Change the color scheme of Slender.
    # See above for preview and list of color schemes.
    colorscheme = "white"

    # Tagline; HTML accepted here. Keep it concise.
    tagline = "Your Tagline"

    # copyright, see http://creativecommons.org/
    licenses = "by-nc-sa"

    # Description and keywords for <meta> tags.
    # Remember to set this for your main page.
    # This will be overridden by whatever is set by the page or post,
    # defined by `description` and `keywords` variables in the front matter
    # of the markdown file.
    description = "Default Page Description"
    keywords = "default,page,keywords"

    # Analytics
    # Remove, comment, or leave it blank if you don't have one.
    googleAnalytics = "GoogleAnalyticsParams"
    baiduTongji = "BaiduTongji"

    # comment
    duoshuoShortname = "your-duoshuo"
    disqusShortname = "you-disqus"

    # MathJax
    # see: http://mathjax.readthedocs.org/en/latest/options/hub.html
    mathjax = true # enable
    mathHideMenu = false
    mathZoom = "Double-Click"
    mathRenderer = "SVG"

[menu]

    # Menu for the nav bar.
    # There must always be one item present (e.g. home).
    # identifier: Font Awesome icon name
    [[menu.main]]
    identifier = "fa-home"
    name       = "Home"
    url        = "/"
    weight     = 0

    [[menu.main]]
    identifier = "fa-user"
    name       = "About"
    url        = "/about/"
    weight     = 1

    [[menu.main]]
    identifier = "fa-archive"
    name       = "Archive"
    url        = "/archive/"
    weight     = 2

    [[menu.main]]
    identifier = "fa-tags"
    name       = "Tags"
    url        = "/tags/"
    weight     = 3
```

### Usage 

**Making a new post / article**

```none
$ hugo new post/hello.md
```

**Making a new page**

```none
$ hugo new page/about.md
```

Add the new page to navbar in `config.toml` under `[menu]`.

### License

[MIT](LICENSE.md) &copy; 2015 CrimsonRay

[MIT](LICENSE.md) &copy; 2016 Neil Shen
