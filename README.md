# ulaval-damas.github.io
[![Build Status](https://travis-ci.org/ulaval-damas/website.svg?branch=master)](https://travis-ci.org/ulaval-damas/website)


### Change website content
To add content, modify the file [index.md](https://github.com/ulaval-damas/website/blob/master/index.md)

#### People
To change the list of people, modify the file [people.yml](https://github.com/ulaval-damas/website/blob/master/_data/people.yml)

#### References
To add or remove references, simply edit [references.bib](https://github.com/ulaval-damas/website/blob/master/_bibliography/references.bib)


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

### Setup `GITHUB_TOKEN` for deployment
If the member that created the deployment token leaves the ulaval-damas
organization, it can break the Travis deployment. A new token needs to be generated. 
Here are the steps generated a new token:

- Create a new Github [Personal Access Token](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/).
- Go to the https://travis-ci.org/ulaval-damas/website/settings
- Delete the old environment variable `GITHUB_TOKEN`
- Add a new environment variable with key `GITHUB_TOKEN` and paste your newly generated token in the value field.

### Setup FSG credentials for deployment
At https://travis-ci.org/ulaval-damas/website/settings, you need to set the environment variables `FSG_USERNAME` and `FSG_PASSWORD` to deploy to the samba server of the FSG.
