# npq hugo theme

![screenshot](https://raw.githubusercontent.com/saadnpq/npq-hugo/master/images/screenshot.png "screenshot")

## main features
- dark
- responsive
- out of the box contact form
- avatar support
- syntax highlighting
- font awesome
- table of content
- customizable

## installation
after you have installed hugo (see [quick start](https://gohugo.io/getting-started/quick-start/)) run the following in your site's root directory to install the theme

```sh
git clone https://github.com/saadnpq/npq-hugo.git
cp npq-hugo/config.toml .
```

## configuration 
this is how your config.toml will look like after installation, change the values according to your site. 

```toml
baseURL = "https://www.example.com"
languageCode = "en-us"
title = "title"
copyright = "Copyright © 2008–2019, Steve Francia and the Hugo Authors; all rights reserved."
theme = "npq-hugo"
pygmentsUseClasses=true

[params]
  author = "your name"
  description = "your description"
  keywords = "hugo blog"
  useAvatar = true
  microBlogSection = "posts"
  displayMicroBlog = true
  displayRecent = true
  recentMax = 4
  mail = "mail@example.com"
  phone = "8888888888"
  formspreeID = "yourformspreeID"

[menu]
  [[menu.main]]
    name = "home"
    pre = "<i class=\"fas fa-home fa-sm\"></i>"
    url = "/"
    weight = -9 
  [[menu.main]]
    name = "blog"
    pre = "<i class=\"fas fa-keyboard fa-ms\"></i>"
    url = "/blog/"
    weight = -8
  [[menu.main]]
    name = "tags"
    pre = "<i class=\"fas fa-tags fa-ms\"></i>"
    url = "/tags"
    weight = -7 
  [[menu.main]]
    name = "github"
    pre = "<i class=\"fab fa-github fa-ms\"></i>"
    url = "https://github.com/yourgithubusername23434"
    weight = -6 
  [[menu.main]]
    name = "RSS"
    pre = "<i class=\"fas fa-rss fa-ms\"></i>"
    url = "/index.xml"
    weight = -4 
  [[menu.main]]
    name = "contact"
    pre = "<i class=\"far fa-envelope\"></i>"
    url = "/contact"
    weight = -1 

```
for the contact page to work you have to make a free form at [formspree](https://formspree.io/) and put your form id in the variable `formspreeID` in the configuration file.

every menu entry has a corresponding section named `[[menu.mail]]` under `[menu]`. to add or change a menu entry add or change the corresponding section with `name` being the name displayed in the menu, `pre` is a text before the name (you can grap icons from [fontawesome](https://fontawesome.com/)), `url` is the url that the menu item points to, and weight is an integer value that represent the order of the menu items (items with lower weight float)

In order to see your site updating while changing it, run Hugo's built-in local server.

```sh
hugo server
```

## License
GPLv3
