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

### Setup `github_token` for deployment
If the member that created the deployment token leaves the ulaval-damas
organization, it can break the Travis deployment. A new token needs to be generated. 

The `github_token` used for deployment is saved as an encrypted environment
variable inside `.travis.yml`. Here are the steps generated a new token:

- Create a new Github [Personal Access Token](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/).
- Delete the `env` section in `.travis.yml`.
- `gem install travis`
- `travis login --org --auto`
- `travis encrypt GITHUB_TOKEN=<insert token here> --add`
