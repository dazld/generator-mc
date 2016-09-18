# Pebble

## What's this?

This is a yeoman generator for making express & js applications. It's the little sister of a fully universal / isomorphic generator which you can find here: https://github.com/dazld/generator-cairn - if you're looking for server rendered react, redux etc, that would be a better place to look. 

There is a full suite of watching, livereloading, compilation and related gulp tasks. The express server renders html as you would expect, and they can be found in the `server/views` folder.

It is a work in progress, and pull requests are welcome as long as they remain in the spirit of the generator.

## Features

- HTTP / HTTPS self signed localhost dev environment including live reload
- full suite of gulp tasks
- watchify accelerated browserify builds
- libsass sass compilation
- eslint rules
- scss lint rules
- babel es2015 / react / object spread
- etc

## Installation

Install Yeoman - `npm install -g yo`.

Install generator globally: `npm install -g generator-pebble`

Check everything is working: `yo --help` - should see a list of generators, and `pebble` in there too.

## Usage

Make a new directory, cd into it.

`yo pebble` - give the project a name (it uses the directory name as default).

Yeoman will perform `git init` and `npm install` for you - this takes a while, so be prepared for a short wait.

`gulp` - default task runs dev server, watches and builds.

`USE_HTTPS=true gulp` for running a *https* localhost server


## Notes

Sockets on iOS with a self signed cert - https://blog.httpwatch.com/2013/12/12/five-tips-for-using-self-signed-ssl-certificates-with-ios/

## Todo

- Document other gulp tasks
- Document how config gets propagated from server render to frontend
- Put skeleton react app in place

## Updating

`npm install -g generator-pebble`


# Changelog

## 1.2.7

- change from `path.join` to `url.resolve` in asset-path helper (windows support)
- Moved `snakeoil-certs` to production dependencies
- added default Node engine (6.3.0)
