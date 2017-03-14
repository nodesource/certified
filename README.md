certified
================================================================================

How to get up-and-running with NodeSource Certified Modules!

Setup
================================================================================

1. Create an account at https://platform.nodesource.io
2. Copy the REGISTRY URL for your account from the bar near the top.
3. run `npm config set registry https://yourregistry.nodesource.io`
4. run `npm ping`, which should print a simple JSON object, to validate you have network access to the repository
5. run `npm login`
  * use anything for username (it's ignored)
  * use the email address you signed up with at https://plaform.nodesource.io
  * use the password you chose upon signup
6. run `npm whoami`, which should print your email address, to validate you have logged in successfully
7. now any `npm install` will use your certified modules registry to screen for quality

Overriding Certification Scores
================================================================================

Sometimes you need a package that fails certification. To do this we provide a tool to curate your NodeSource Certified Modules' whitelist. This list overrides any certification criteria failures and allows `npm` to install packages that it would otherwise prevent.

For the `nscm` tool and its documentation, check out https://npmjs.org/package/nscm

Advanced Setup
================================================================================

You can leverage `.npmrc` files per folder to allow easier control of which registry is being used for a project. This is convenient if you work on open source modules but don't want to have to switch your registry back and forth between NodeSource Certified Modules and the npmjs.org registry.

1. Create a `.npmrc` file in your project folder
2. in the `.npmrc` file, add the line: `registry = https://yourregistry.nodesource.io`
3. `chmod 0600 .npmrc`
4. `npm login` as above (if not already logged in to this registry)

How To Switch Back To The npmjs.org Registry
================================================================================

Currently publishing is not supported by NodeSource Certified Modules, so you will need to switch back to the https://npmjs.org registry whenever you want to publish a module. If you do this a lot, you may want to consider the advanced setup using `.npmrc` files.

1. run `npm config set registry https://registry.npmjs.org/`
2. run `npm login` and use your npmjs.org credentials

Contributing
================================================================================

To submit a bug report, please create an [issue at GitHub][].

If you'd like to contribute code to this project, please read the
[CONTRIBUTING.md][] document.


License & Copyright
================================================================================

**certified** is Copyright (c) 2017 NodeSource and licensed under the
MIT license. All rights not explicitly granted in the MIT license are reserved.
See the included [LICENSE.md][] file for more details.


[issue at GitHub]: https://github.com/nodesource/nsolid-statsd/issues
[CONTRIBUTING.md]: CONTRIBUTING.md
[LICENSE.md]: LICENSE.md
