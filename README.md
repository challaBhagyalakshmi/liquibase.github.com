# liquibase.github.io

Documentation for the liquibase.org site.

***Please send pull requests!***

## Project Overview

The Liquibase site is hosted using GitHub Pages, and generated using [Jekyll](http://jekyllrb.com/). Pages are written in MarkDown documents, making use of [Liquid template tags](http://jekyllrb.com/docs/templates/).

To build the site for local testing, install Jekyll and its dependencies, including Ruby, the kramdown gem, Python 2.7, and the Pygments package. If you're developing on Windows, there is a handy [Portable package of Jekyll](https://github.com/madhur/PortableJekyll) you can use. You may still need to fiddle around a bit to get it working, such as installing the kramdown gem ("gem install kramdown") and editing "setpath.cmd".

Once Jekyll is installed, just navigate to this repo's directory, and run `jekyll serve`. You can then access the site from `http://localhost:4000`.

If you're using a MarkDown editor with a "live preview" feature, be aware that it's unlikely to support Liquid's syntax highlighting tags, such as "{% highlight xml %}".

## Project Setup
### Requirements (Bundler)
* [Ruby](https://ruby-doc.org/)
  * _OR_ [RVM](https://rvm.io/rvm/install)
* [Bundler](https://bundler.io/)

### Steps
#### Bundler
##### Install
Once all requirements are met, you can install everything with:
```bash
bundle install
```

##### Local Dev Server
```bash
bundle exec jekyll serve 
```
_Or_
```bash
bundle exec jekyll serve -l
```
The -l option specifies "live reload" to automatically refresh your browser when a content change is complete.

#### Local Server
To access the local development server navigate to: `0.0.0.0:4000` (the default Jekyll port).

### Requirements (Docker)
Or if you'd prefer to run everything through a docker container:
* [Docker](https://www.docker.com/)

#### Docker
```bash
./scripts/docker-dev.sh
```

### CI/CD Overview
#### Staging (staging.liquibase.org)
To see your changes in a `staging` environment, base your PRs on the `staging` branch. When the PR is merged to staging, a build server will 
generate the site and publish it to http://staging.liquibase.org/ within about 10 minutes. After review by the team, staging will be merged to master
typically within 1 business day. 

#### Production (liquibase.org)
To see the changes in `production` a merge must be made into `master`. GH Pages will handle the deployment.
