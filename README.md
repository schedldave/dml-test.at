# Website for digitalmedialab.at

[Jenkyll Website](https://jekyllrb.com/) for the Digital Media Lab (DML) research group, online at [digitalmedialab.at](digitalmedialab.at). The domain is registered with World4You and hosted on GitHub-Pages. The setup is such that every change in the repository is directly applied online by GitHub-Pages. Content is stored file-based: mostly Markdown (.md) and YML (.yml) files.

## Notes on the Setup

`_sass` and `_js` contain the source files. The `css` and `js` folders and their content are only held in this repository to provide them for gh-pages. These tasks aren’t included in the Jekyll build itself, so setting up a development machine is recommended. See the instructions for Windows and Mac OS X below.

# Local Development

If you want to make considerable changes to the website please test them first with a local setup.

These are the complete instructions for a development machine running under Microsoft Windows. The instructions should be very similar for any other operating system.

### Install Git and Clone the Repository

Get the Git binaries from [https://git-scm.com/](https://git-scm.com/) or download GitHub Desktop from [https://desktop.github.com/](https://desktop.github.com/), then clone the repository to your local machine (e.g., `C:\Users\[User]\Documents\GitHub\digitalmedialab.at`).

### Install Ruby

Go to [http://rubyinstaller.org/](http://rubyinstaller.org/), download the latest installer for Ruby (Ruby+Devkit) and run it.

### Install Bundler and Jekyll

Once Ruby is installed, install Jekyll and its necessary plugins using [Bundler](https://bundler.io/). First, install the Bundler gem: `gem install jekyll bundler`. Then install the gems listed in the Gemfile by calling `bundle install`. For the later command you need have the repo in the current working path.

For further details, see [https://jekyllrb.com/docs/installation/](https://jekyllrb.com/docs/installation/).

### (Not needed anymore!?) Install Node.js

Node.js is used for the Gulp build workflow and to compile SASS (and other things). Go to [https://nodejs.org/](https://nodejs.org/) and download the current version and install it. The LTS version (usually older) is not required.

### (Not needed anymore!?) Install the Dependencies for the Build Process

First, install the Gulp.js CLI globally: `npm install gulp-cli -g`.
Open a Terminal window and go to the directory where you cloned the repository (e.g., `C:\Users\[User]\Documents\GitHub\pie-lab.at`). Type in `npm install` to install all necessary dependencies.

### Start the Build System

The build workflow then uses bundle and can be started with: `bundle exec jekyll serve`.
A local server should be running at the address http://127.0.0.1:4000 and can be used to preview the website. Any changes and additions to markdown files should be imediatly visible. Note that changes to `_config.yml` need a restart of the build system!

## Updating Dependencies

The packages used throughout the site are from the Ruby (gem) and Node.js (npm) ecosystems. They need to be updated separately.

To update all Ruby gems involved, run `bundle update`. To remove (now unused) older versions, type `gem cleanup`.

## (Not needed anymore!?) Update Node.js Dependencies

To update all Node.js modules involved, run `npm update`.

To go a step further and upgrade all dependencies in `package.json` to their latest available versions, use `npm-check-updates -u` (install first if not available: `npm install -g npm-check-updates`). This will create an updated `package.json`. Ensure that the previous version is stored in version control since npm-check-updates will overwrite it.

# Acknowledgements

This website is based on the pie-lab website designed, developed and maintained by Thomas Heller and Wolfgang Hochleitner among others. Thanks to them for the great work and the permission to use their code as a starting point for this website!
