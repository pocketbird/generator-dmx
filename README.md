# DMX

DMX is a Yeoman generator to get you building interfaces faster. [Jekyll](http://jekyllrb.com/) is included for static site generation. [Bootstrap](http://getbootstrap.com) is included to help you build your site quickly.

[Grunt](http://gruntjs.com/) is used for compilation of [Less](http://lesscss.org/) and [CoffeeScript](http://coffeescript.org) (optional). [Bower](http://bower.io/) is used for managing dependencies.

### Prerequisites
If you do not have [Node.js](http://nodejs.org/) `>=0.10`, [Yeoman](http://yeoman.io/) `>=1.1.2`, [Ruby](https://www.ruby-lang.org/en/) `>=1.9` and the [Bundler](http://bundler.io/) gem installed, you must do that first:

- [Node.js](https://nodejs.org/en/)
- [Yeoman](http://yeoman.io/learning/index.html)
- [Ruby](https://rvm.io/rvm/install)
- [Bundler](http://bundler.io/#getting-started)

### Installation
````bash
npm install -g generator-dmx
````

### Update

If you already have generator-dmx installed, please upgrade before
generating another site to get the latest updates.

```bash
npm list -g | grep 'generator-dmx' # See your installed version
npm info generator-dmx | grep 'latest' # See latest generator-dmx version
npm update -g generator-dmx # Upgrade generator-dmx globally
```

### Usage
DMX will run `bundle install`, so if you would like to install the DMX gems into a gemset, set that up before running `yo dmx`.

````bash
mkdir project-name && cd project-name
yo dmx
````

*Should you run into an error such as `command yo not found` it may be related to a path issue when installing Node.js via Homebrew. Please refer to the top answer on this [StackOverflow question](http://stackoverflow.com/questions/15846076/command-not-found-after-installation).*

### Grunt Tasks
##### grunt serve
Serve your source locally into your browser. LiveReload will automatically load any changes to HTML, CSS and JavaScript that you make.

##### grunt check
Check the quality of your source with tools like [JSLint](http://www.jslint.com/), [CSSLint](http://csslint.net/) and [csscss](http://zmoazeni.github.io/csscss/).

##### grunt build
Build the concatenated, minified production version of the source into the `dist` directory.

##### grunt deploy
Deploy the production version of the source to [GitHub Pages](http://pages.github.com/). This ability is configurable during dmx generation.

If you choose to utilize `grunt-build-control` to deploy a GitHub Pages user/organization site, your source must live in a branch other than `master`. GitHub Pages [user/organization sites](https://help.github.com/articles/user-organization-and-project-pages#project-pages) serve the files found in the `master` branch to the browser.
