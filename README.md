# Kaiyuan's Personal Website

## Tutorials 

[Building an Academic Website](https://jayrobwilliams.com/posts/2020/06/academic-website/), [Test site locally](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll)

Template resources: [Academic Pages](https://github.com/academicpages/academicpages.github.io), [Weightshift, the personal page](https://github.com/kylewang1999/kylewang1999.github.io.git), [GitPage tutorial](https://pages.github.com/#project-site)

- This website uses the template from [Academic Pages](https://github.com/academicpages/academicpages.github.io).
- [README: Academic Pages](./README_academicpages.md)

**Render and serve the website on localhost**: `bundle exec jekyll serve` 

## Entry Points

- [Top navigation bar](./_data/navigation.yml): [Teaching](./_teaching/), [CV](./_pages/cv.md), [Publications](./_publications/), [Learn with me](./_learn_with_me)
- [Home page](./_pages/about.md)
- [Side author bar](./_config.yml)
- [Footer](./_includes/footer.html)


---
## Env Setup 

[Node js on M1 mac](https://www.jurnalanas.com/node-js-mac-m1/), [Jekyll on M1 Mac](https://www.earthinversion.com/blogging/how-to-install-jekyll-on-appple-m1-macbook/) 

Install [Jekyll](https://jekyllrb.com/docs/installation/) (Ubuntu).
```bash
# Install Ruby and other pre-req
sudo apt-get install ruby-full build-essential zlib1g-dev # ubuntu

# Avoid installing RubyGem as root. Instead, set up gem install dir for the user.
# The following adds environment vars to ~/.bashrc to configure gem install path
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc

# Install Jekyllm Bundler
gem install jekyll bundler && bundle install 
```


Set up environment (MacOS)
```bash
rbenv install 3.0.0     # Install arm-based ruby 3.0.0
rbenv global 3.0.0
ruby -v
rbenv rehash

echo 'eval "$(rbenv init - bash)"' >> ~/.bash_profile   # if using bash

gem install --user-install bundler jekyll

ruby -v     # Check ruby version, substitute in the following line
echo 'export PATH="/usr/local/opt/ruby/bin:/usr/local/lib/ruby/gems/3.0.0/bin:$PATH"' >> ~/.bash_profile

bundle update --bundler
bundle add webrick
bundle install --redownload
```


Export `nvm` ot environment variable:

```bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
```

---

## Bug Log

Webrick cannot be found. [Solution](https://github.com/jekyll/jekyll/issues/8523).

---

## [Academic Pages Guide](./_pages/markdown.md)

* Basic config options: `_config.yml`
* Top navigation bar config: `_data/navigation.yml`
* Single pages: `_pages/`
* Collections of pages are .md or .html files in:
  * _publications/
  * _portfolio/
  * _posts/
  * _teaching/
  * _talks/
* Footer: `_includes/footer.html`
* Static files (like PDFs): /files/
* Profile image (can set in _config.yml): `images/profile.png`