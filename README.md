grunt-source-ghpages
====================

A GruntSource project to build Github Pages websites

## Usage


* Install Grunt Source

  ``` shell
  npm install -g grunt-source grunt-cli
  ```

* Create a `Gruntsource.json` in your project's root

  ``` shell
  {
      "source": "~/./grunt-sources/ghpages",
      "repo": "https://github.com/jpillora/grunt-source-ghpages.git"
  }
  ```

  *Note: You can change the destination path*

* Create the following directory structure:

  ```
  Gruntsource.json
  src/
      scripts/index.coffee
      styles/index.styl
      views/index.jade
  ```

* Run:

  ```
  grunt-source
  ```

* Poof:

  ```
  Gruntsource.json
  js/app.js
  css/app.css
  index.html
  src/...
  ```

## Features

The default task will:

* Development and Production builds with `--env dev|prod`
* Compile your CoffeeScript, Jade and Stylus
* Watch source each directory and compile only what is required

The current setup will create 1 JS, 1 CSS, 1 HTML in an effort to reduce the asset count. You can use any number of `.coffee` files as they will all be joined and wrapped in an IEFF, you can use more `.styl` files by using the built-in `include` syntax, and similarly, you can use the built-in `include` to split out your HTML into a logical file structure of `.jade` files. See the [verifyjs.com repo](https://github.com/jpillora/verifyjs-com) for an example of this.

## Customising

Replace the `source` directory with your fork of the
[grunt-source-ghpages repo](https://github.com/jpillora/grunt-source-ghpages) and
edit your `GruntSource.json` file's `repo` to be the new Git URL - then rerun `grunt-source`.

