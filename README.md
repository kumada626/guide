# Screwdriver Guide
[![Build Status][status-image]][status-url] [![Open Issues][issues-image]][issues-url]

## Installation of Jekyll
In order to install Jekyll you'll need Ruby installed on your system, as well as the Ruby package manager, RubyGems.
And you need to install bundle to install and run Jekyll.
You can check if you have these already installed like so:

```bash
$ ruby --version
ruby 2.4.1
$ gem --version
2.6.12
$ bundle --version
Bundler version 1.15.1
```

Jekyll supports Ruby version 2.1 or above.

### Standard

To install the `jekyll` using bundle, making sure we're in the same directory as the `Gemfile`.

Install the `jekyll` package using bundler:

```bash
bundle install
```

You should now have the `jekyll` command installed on your system. Run `bundle exec jekyll --version` to check that everything worked okay.

```bash
$ bundle exec jekyll --version
jekyll 3.5.0
```

## Viewing docs locally
There's a single configuration file named `_config.yml`, and a folder named `docs` that will contain our documentation source files.

Jekyll comes with a built-in webserver that lets you preview your documentation as you work on it. You can start the webserver locally with Jekyll directly.

### Standard

Jekyll comes with a built-in webserver that lets you preview your documentation as you work on it. We start the webserver by making sure we're in the same directory as the `docs` folder, and then running the `bundle exec jekyll serve --source docs --destination _site` command:

```bash
$ bundle exec jekyll serve --source docs --destination _site
Configuration file: docs/_config.yml
            Source: docs
       Destination: _site
 Incremental build: disabled. Enable with --incremental
      Generating...
                    done in 2.251 seconds.
 Auto-regeneration: enabled for 'docs'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```

### Browse your local guide

Once you successfully start the webserver, open up [http://127.0.0.1:4000/](http://127.0.0.1:4000/) in your browser. You'll be able to see the index page being displayed.
And you'll also be able to see the other language index page open up http://127.0.0.1:4000/:lang/ in your browser.
For example, open up [http://127.0.0.1:4000/ja/](http://127.0.0.1:4000/ja/) in your browser, you'll be able to see the Japanese index page being displayed.

## Adding docs
Simply add a new markdown document to the folder hierarchy in `docs`, and add an entry to the tree in `docs/_data/menu.yaml`

## Documentation Structure

- Homepage
  - [x] What are the sections for
- Cluster Management (for SD owners)
  - [x] Overall architecture
  - [x] Running locally
  - [x] Configuring API
     - [x] Scm plugins
     - [x] Datastore plugins
  - [x] Configuring UI
  - [x] Configuring Store
     - [x] Logging plugins
  - Examples
    - [x] Setting up Kubernetes
  - [ ] Debugging
- User Guide
  - [x] Quickstart
  - [x] Configuration
    - [x] Overall YAML
    - [x] Secrets
  - [x] API
  - [x] Authentication and Authorization
- About
  - [x] What is SD?
  - [x] Appendix
    - [x] Execution engines
    - [x] Domain model
  - [x] Contributing
  - [x] Support


[issues-image]: https://img.shields.io/github/issues/screwdriver-cd/screwdriver.svg
[issues-url]: https://github.com/screwdriver-cd/screwdriver/issues
[status-image]: https://cd.screwdriver.cd/pipelines/27/badge
[status-url]: https://cd.screwdriver.cd/pipelines/27
