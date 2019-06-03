---
layout: post
title:  "Meta 1: Discovering Jekyll"
date:   2019-06-02 
categories: blog jekyll meta 
author: Gabriel Kwan
exerpt: Welcome to the first blog post of this Jekyll generated website.
---

Welcome to the first blog post of this Jekyll generated website.

## Boredom

Having just finished finals,  I decided to try my hand at blogging, or at least configuring it. What I was looking for was a way of generating a blog/website using plain text. Ideally, it would be done with org documents.  

## o-blog

The first project I decided to take a look at was [o-blog](http://renard.github.io/o-blog/). Having used Emacs Org-Mode and Evil mode for notes taking initially wanted to use something integrated with emacs.  O-blog was the first project suggested on the [Blogs and Wikis with Org](https://orgmode.org/worg/org-blog-wiki.html) site.
  
Neither automatic installation using el-get nor manually cloning the git repositories did worked. When looking up the error, users on the project issues page state that it does not work with Emacs version 25. The Latest version it works with is version 24. There did not seem to be any package for Emacs 24 in the repository (Elementary OS Juno) and I was not sure if it installing it alongside version 25 would cause issues.

Furthermore, o-blog is not longer in active development. A fix for version 25 seems unlikely. The issue posts I referenced were from 2017 and the last commit was 4 years ago as of writing this post.

## Jekyll and Visual Studio Code

As such, I decided to try Jekyll. Installation was straight forward.
Only prerequisites were ruby. Being a fresh os install, I simply ran the command suggested for Ubuntu as seen below:

``` Bash
# Install ruby and prerequsites
sudo apt-get install ruby-full build-essential zlib1g-dev

# Appending paths for local user, also modified ~/.bashrc to ~/.zshrc
echo '# Install Ruby Gems to ~/gems' >> ~/.zshrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.zshrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.zshrc

# Source configuration file to make previous commands take effect
source ~/.zshrc
```

Although there is a package that enables Jekyll integration with org documents, it works by default with markdown or HTML. So, in the spirit of trying new things, I took the opportunity to try working with Visual Studio Code. Friends have been telling me how great it and I have yet to use in in extensive manner.

Thus far, its been quite comfy and adjusting has been made easier the Vim extension. The default themes seem good enough. More thoughts on it once I get some more time with it. I might still end up going back to Emacs due to the lack of shortcuts for org in VSC.

### Initial Configuration

Made modifications to _config.yaml, created an additional [Projects](/projects/index.html) page and created wrote this post. Also fixed some hyperlinks to some PDFs on the [About](/about/index.html) page.
Check <https://github.com/fumofu/mywebsite> for more details.

### Future Configuration

While the default theme is clean, an "about me" panel on the left or right side of the page would be desirable. It just seems like there is a lot of empty space. That may require digging deeper into the documentation and brushing up on ruby modify default theme to enable this.
