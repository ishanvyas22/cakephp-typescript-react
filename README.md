# CakePHP + Typescript + React Application Skeleton

An application skeleton for creating applications with
[CakePHP](https://cakephp.org) 4.x, typescript and react.

## Installation

1. Download [Composer](https://getcomposer.org/doc/00-intro.md) or update `composer self-update`.
2. Ensure youh 
3. Run `php composer.phar create-project --prefer-dist markstory/cakephp-typescript-react [app_name]`.
4. Install nodejs dependencies with `npm install` or `yarn install`.

## Running the local PHP server

You can run the local PHP server with:

    bin/cake server

And then visit this server at `http://localhost:8765`. Using another webserver
is possible, but you will need to further configure `mix` to know about the subdirectory
your application is running in.

## Frontend Assets

Unlike typical CakePHP applications, the frontend assets in this skeleton live
in `assets`.  In this directory you'll find directories for the
[SASS](https://sass-lang.com) and [Typescript](https://typescriptlang.org) files
your application will use. These source files are compiled into assets stored in
`webroot` via [webpack](https://webpack.js.org).

## Running webpack

This skeleton uses [mix](https://laravel-mix.com/docs/6.0/installation) as
a high-level wrapper around webpack to build the typescript/react & sass assets.
For local development you'll generally want to run webpack in 'watch' mode:

    yarn run watch

In watch mode, webpack will watch the filesystem for changes and recompile as necessary.
Source maps will be available in watch mode.

When it comes time to deploy your application to production you should use:

    yarn run build

The above will generate minified assets and *not* generate sourcemaps. Ideally
the above command is generated during your deploy process, or when you build the
artifacts you are going to deploy.