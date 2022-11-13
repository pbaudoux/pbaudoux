---
layout: post
title:  "Welcome to Jekyll!"
date:   2022-06-11
modified_date: 2022-06-15
category: misc
tags: jekyll website
---

This website uses [Jekyll](https://jekyllrb.com/docs/) to easily turn plain text into a static website, and is hosted on [GitHub pages](https://pages.github.com/).

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file (`md` for Markdown). After that, include the necessary front matter.

This command builds the website and serves it at [http://localhost:4000/](http://localhost:4000/)
{% highlight shell %}
bundle exec jekyll serve --livereload
{% endhighlight %}

Some of the customizations from the default Jekyll theme (minima) are inspired from [here](https://simonkjohnston.life/code/2019/07/08/Some-Jekyll-Customization.html) and [there](https://ouyi.github.io/post/2017/12/23/jekyll-customization.html).
