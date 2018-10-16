# Personal Website

[![CC BY 4.0][cc-by-shield]][cc-by]

This repo contains my personal website. It is developed in
[Jekyll](https://jekyllrb.com/), hosted
by [GitHub Pages](https://pages.github.com/) and built upon
[Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/)
who aids anyone to create its own personal website without
learning CSS nor HTML.

## How to run it locally

Clone the repo to your computer:

    git clone https://www.github.com/santis19/santis19.github.io/

Or download it from
[here](https://github.com/santis19/santis19.github.io/archive/master.zip).

### Install dependencies

#### Debian 9

First install ruby development environment and essential tools for building:

    sudo apt-get install ruby-dev build-essential zlib1g-dev

Then install Jekyll and Bundler through Gem:

	sudo gem install jekyll bundler

Check that the directory `~/.bundler` is owned by the user and not the root.
If it's owned by root, run the following:

    cd ~
    sudo chown -R <user-name> .bundle
    sudo chgrp -R <user-group> .bundle

Go to the cloned repo:

    cd /path/to/santis19.github.io

And run `bundle install` or use the Makefile targets:

    make install

### Manjaro

Install ruby:

    sudo pacman -S ruby

Add the following lines to your `.bashrc` or to you specific `bash`
configuration files:

    PATH="$PATH:$(ruby -e 'print Gem.user_dir')/bin"
    export GEM_HOME=$HOME/.gem

These allows your user to install and run gems without inserting the full
location.

Then run:

    make install


### Start serving the website

Simply run `make serve` to start serving the website locally.
In order to see it open your favorite web-browser and go to:

    localhost:4000

If it doesn't work, try the url shown in the prompt, the port may be different.


## License


This content is licensed under a [Creative Commons Attribution 4.0
International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg
