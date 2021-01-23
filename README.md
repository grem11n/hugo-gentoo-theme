# hugo-gentoo-theme
![test-theme](https://github.com/grem11n/hugo-gentoo-theme/workflows/test-theme/badge.svg)
[![Netlify Status](https://api.netlify.com/api/v1/badges/7daab0af-af8d-415c-9d83-f6994bc8b67b/deploy-status)](https://app.netlify.com/sites/laughing-bartik-75b6a3/deploys)

This is a fork of the [hugo-gentoo-theme](https://github.com/d-kusk/hugo-gentoo-theme) theme for [Hugo](https://gohugo.io), which is archived now.
This theme has a motif of Gentoo penguin.

![hugo-gentoo-theme's screenshot](https://raw.githubusercontent.com/grem11n/hugo-gentoo-theme/master/images/screenshot.png)

## Features

- Responsive Design
- Support for tags and categories
- Support of [Google Analytics](https://analytics.google.com/analytics/web/provision/#/provision) via Hugo [configuration file](https://gohugo.io/getting-started/configuration/) file
- Support of the social links
- Support post image thumbnails

## Preview the theme

For a live demo of this theme you can visit:
- [hugo-gentoo-theme.netlify.app](https://hugo-gentoo-theme.netlify.app)
- [grem1.in](grem1.in)

You can also preview this theme locally. It is shipped with a fully configured example site. For a quick preview clone this repository and execute:

```
$ cd exampleSite/
$ hugo serve  --themesDir ../..
```

## Usage

### Installation

Before installing this theme, be sure to [install Hugo](https://gohugo.io/getting-started/quick-start/)
and [create a new site](https://gohugo.io/getting-started/quick-start/#step-2-create-a-new-site).

To install the theme, run the following from the root directory of your Hugo site:

```
$ git submodule add https://github.com/grem11n/hugo-gentoo-theme.git themes/hugo-gentoo-theme
```

With a submodule you will be able to easily update the theme. However, you can also just download the repository contents and put it into your `themes/` directory for your Hugo website. You can modify this theme for your needs as well.

### Configuration

You need to modify your `config.toml` file in the root of your Hugo website. An example `config.toml` for Gentoo theme is listed below. Depends on your hosting provider some of the general parameters may be different.

```toml
baseURL = "https://example.com"
title = "Your Website Title"
languageCode = "en-us"
theme = "gentoo"
googleAnalytics = ""

copyright = "&copy; Copyright Year, Your Name"
canonifyurls = true
paginate = 6

[params]
  description = "This website is using Gentoo theme"
  author = "Youe name"

  # mainSections configures, pages from which sections will be listed on the main page
  mainSections = ["post", "posts"]

[taxonomies]
  # categories are rendered in top menu
  category = "categories"
  tag = "tags"
  series = "series"


# You can also configure static pages on your website.
# to make it work, you need to have corresponding subdirectory under content/ dir with index.md
# In this particular case it would be:
# content/about/index.md
#
[[menu.global]]
    name = "About"
    url = "/about/"

# You can configure links to your social media
[params.social]
    twitter       = ""
    github        = ""
    telegram      = ""
    email         = ""
    linkedin      = ""
    stackoverflow = ""
```

### Updating

To get updates to the theme, run the following from the root directory of your Hugo site: 

```
$ git submodule update --remote themes/hugo-gentoo-theme
```

### Preview your site locally

Use Hugo’s built-in server to see your site in action as you make changes.

```
$ hugo server -D -w --gc -F -t hugo-gentoo-theme
```

After that visit ``localhost:1313`` in your browser.

### Add image thumbnails to your posts

To create a new blog post, run:

```
$ hugo new post/your-post-name.md
```

To add an image thumbnail to the post, add `image` parameter with a link to the image. Example of the configuration:

```yaml
---
title: "Article"
description: "Lorem ipsum"
date: 2021-01-01
draft: false
slug: "article"
image: "https://example.com/img/picture.jpg"
categories: ["Blog"]
tags: ["gentoo", "theme", "hugo"]
---
```

### Arrange images on a page

You can arrange images on a page to move them to the left, right, or in the center of a page. Image placed on the right hand side by default. To change its position, add a `class` parameter like on example below:

```
{{< figure src="/img/picture.jpg" class="left" >}}
```

### Netlify

You can connect to Netlify and deploy your site by just pressing this button!

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/grem11n/hugo-gentoo-theme)

## Contributing

If you have an idea on how to improve this theme or found a bug feel free to use [GitHub issues](https://github.com/grem11n/hugo-gentoo-theme/issues) to let me know.

If you want to contribute to this theme, please, fork this repository and create a pull request.

## License
This theme is released under the [MIT license](https://github.com/grem11n/hugo-gentoo-theme/blob/master/LICENSE.md)
