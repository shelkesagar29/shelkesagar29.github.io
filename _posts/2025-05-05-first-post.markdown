---
layout: post
title:  "Getting Started and Jekyll!"
date:   2025-05-05
tags: [Technology]
---
Today, I finally decided to start writing notes about the technical topics I study, my travels, and other experiences in life — something I’ve been meaning to do for a long time.

A quick GPT search on how to create a GitHub Pages–based blog led me to [Jekyll](https://jekyllrb.com/), a static site generator. What appealed to me most was the ability to write content in Markdown instead of HTML/CSS. I appreciate Markdown for its simplicity, yet it’s powerful enough to structure content effectively. In this post, I’ll share how Jekyll helped me get started with building a simple yet effective blog site.

Jekyll needs Ruby which is preinstalled on mac.

### Pre-requisite
1. Install Ruby, if not installed already.
```
ruby -v # Should tell Ruby version
```
2. Install bundler.
```bash
sudo gem install bundler
```
In Ruby, a `gem` is a package of reusable code (like Python packages on PyPI). These are hosted at RubyGems.org. `Bundler` is Ruby’s package manager — similar to pip in Python — and is itself a gem used to manage other gems. You define required gems in a `Gemfile`, and install them using:
```bash
bundle install
```

3. Install Jekyll
```bash
gem install jekyll
```  

After this, we are ready to use Jekyll magic!!


### Getting Started
1. Create an empty repo on GitHub. If you are planning to use GitHub pages, name must be
`yourusername.github.io`.

2. Clone the repo and navigate to it.
```bash
git clone https://github.com/yourusername/yourusername.github.io
cd yourusername.github.io
```

3. Create new Jekyll site. 
```bash
jekyll new . --skip-bundle
```  
This will create project with `minima` theme, by default.

4. Serve the Site Locally,
```bash
bundle install
bundle exec jeklyll serve
```  
Open the local server shown in the terminal. Make changes
to meet your content and styling requirements.

5. Push to GitHub and publish website
After changes you made are working as expected, push local changes to upstream
GitHub repo.
```bash
git add .  # Adds all changes
git commit -m "<your-commit-message>"
git push origin
```  

6. Go to your repository on GitHub.

7. Go to Settings → Pages.
  - Click the "Settings" tab in your repo.
  - In the left sidebar, scroll down and click "Pages".

8. Under “Source”, select your publishing branch
  - Under "Source", choose the branch (usually main).
  - Set the folder to / (root) if your site is in the root of the repo. 

Click `Save` and wait for GitHub to publish your website.

> 💡 **Note:** 
> - If your repo is named exactly like `yourusername.github.io`, the site will be published directly at `yourusername.github.io`.  
> - GitHub Pages automatically builds the site using Jekyll (no need to run jekyll build yourself).  
> - You don’t need to host the `_site/ folder` — GitHub builds it for you.

