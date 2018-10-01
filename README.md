# ulaval-damas.github.io
[![Build Status](https://travis-ci.org/ulaval-damas/ulaval-damas.github.io.svg?branch=master)](https://travis-ci.org/ulaval-damas/ulaval-damas.github.io)


### Work locally

To develop locally this website, you need to install dependencies first:

``` bash
sudo apt install ruby-full
echo 'export PATH=$PATH:~/.gem/ruby/2.4.0/bin >> ~/.bashrc
source ~/.bashrc

gem install jekyll bundler github-pages
```

Then, to have a local web server, run:

```bash
bundle exec jekyll serve --watch
```
