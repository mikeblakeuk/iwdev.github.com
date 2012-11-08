---
layout: post
title: "Website Competition Help"
date: 2012-11-07 12:57
comments: true
categories: 
---

I'm quite aware that the competition has several potential knowledge barriers. I am hoping that it participating will help in learning and installing a few different things (learning is fun, right?) - but I understand that time isn't cheap and we don't all have much of it. So I've put together a little step-by-step how-to to help you on your way. In honesty I've only tested this process on Windows 7 - but I think that it is pretty sound.

<!--more-->

###1. Pre-requisites###

**Ruby 1.9.3 Runtime and Development Environment**

* [Rbenv](http://octopress.org/docs/setup/rbenv/), or
* [RVM](http://octopress.org/docs/setup/rvm/), or
* If you're on Windows it is easier to use [RubyInstaller](http://rubyinstaller.org/) with [The Ruby DevKit](https://github.com/oneclick/rubyinstaller/wiki/Development-Kit). 

###2. Get the IWDev Website from GitHub###

* Go to `https://github.com/IWDev` in your favourite browser.
* Click on the `iwdev.github.com` repository in the list.
* Click on the `Fork` button at the top right - this will copy the entire IWDev website repository to your very own private version of the website.
* Clone your version of the IWDev website down to a local working folder on your computer:
``` 
git clone git://github.com/&gt;your_github_username&lt;/iwdev.github.com.git IWDev-Website
```
* Go into the local working folder:
``` 
cd IWDev-Website/
```
* Double check which version of Ruby you have installed (and double check that it is on your path!) - it should report 1.9.3:
``` 
ruby --version
```
* Install the Bundler Ruby gem:
``` 
gem install bundler
```
* Run the bundler install task:
``` 
bundle install
```
* Generate the website from the source code:
``` 
rake generate
```
* Confirm that it has all worked, running the self-hosting preview server:
``` 
rake preview
```
* Preview the generated website in your favourite browser at `http://localhost:4000/`

###3. Working with Octopress###

Assuming that you're on the `source` branch of the repo, there is a `source/` directory in the root of working folder. In there is everything that you really need to edit: css, javascript, html, includes etc.

Here is a list of useful links to also help you on your way:

* [Theming &amp; Customization](http://octopress.org/docs/theme/)
* [Editing Content (Blog Posts &amp; Pages)](http://octopress.org/docs/blogging/)
* [3rd Party Themes](https://github.com/imathis/octopress/wiki/3rd-Party-Octopress-Themes)
* [3rd Party Plugins](https://github.com/imathis/octopress/wiki/3rd-party-plugins)

...and when you've made changes:

* Generate the website from the source code:
``` 
rake generate
```
* Confirm that it has all worked, running the self-hosting preview server:
``` 
rake preview
```