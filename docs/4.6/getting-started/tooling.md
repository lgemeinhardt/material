---
layout: docs
title: Tooling
description: Learn how to use Material's included npm scripts to build our documentation, compile source code, and more.
group: getting-started
toc: true
---

## Getting started

Material uses [NPM scripts](https://nodejs.org/en/) for its build system. Our [package.json]({{ site.repo }}/blob/v{{ site.current_version }}-{{ site.material_version }}/package.json) includes convenient methods for working with the framework.

To use our build system, you'll need a copy of Material's source code and Node. Follow these steps and you should be ready to rock:

1. [Download and install Node.js](https://nodejs.org/en/), which we use to manage our dependencies. Then navigate to the root `/djibe-material` directory and run `npm install` to install build dependencies.
2. [Download and install Ruby](https://www.ruby-lang.org/en/downloads/), install [Bundler](https://bundler.io/) from a terminal with `gem install bundler`, and then run `bundle install`. This will install all Ruby dependencies, such as Jekyll (static site generator) and plugins.

When completed, you'll be able to run the various commands provided from the command line. Our [package.json]({{ site.repo }}/blob/v{{ site.current_version }}/package.json) includes the following commands and tasks:

| Task           | Description |
| -------------- | ----------- |
| `npm run dist` | `npm run dist` creates the `/css` and `/js` directories with compiled files. |
| `npm run docs` | Builds CSS and JavaScript for docs. You can then run the documentation locally via `npm run docs-serve`. |

Run `npm run` to see all the npm scripts.

## Local documentation

Running our documentation locally requires the use of [Jekyll](https://jekyllrb.com/docs/home/), a decently flexible static site generator that provides us: basic includes, Markdown-based files, templates, and more. Here's how to get it started:

1. Run through the [getting started guide](#getting-started) above to install Jekyll and other Ruby dependencies with `bundle install`.
2. From the root `/djibe-material` directory, run `npm run docs-serve` in the command line.
3. Open `http://127.0.0.1:9999/material/` in your browser, and voilà (or just click on the *Server address* returned by the Terminal).

## PostCSS

Material uses [Autoprefixer](https://github.com/postcss/autoprefixer) (included in our build process) to automatically add vendor prefixes to some CSS properties at build time. Doing so saves us time and code by allowing us to write key parts of our CSS a single time while eliminating the need for vendor mixins.

We maintain the same browsers supported by Bootstrap 4 in our [package.json]({{ site.repo }}/blob/v{{ site.current_version }}/package.json) file.
