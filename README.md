# Apache Ripple(tm)

A browser based, platform agnostic mobile application development and testing tool.
 
## Build Requirements

* OSX / Linux
 * nodejs, npm
* Windows
 * nodejs, npm
 * [Python](https://www.python.org/downloads/) (`v.2.7.x` recommended, `v.3.x.x` is not supported)
 * Visual Studio 2010. The setup instructions can be found [here](https://github.com/brianmcd/contextify/wiki/Windows-Installation-Guide)
 * Ripple uses [Bower](http://bower.io/) for js libraries managing. In order to use Bower on Windows, [msysgit](http://msysgit.github.io/) must be installed in a proper way - see Bower's [README.md](https://github.com/bower/bower#windows-users)

## Getting Started

If you plan to dive into the source, be sure to check out the [HACKING](https://github.com/apache/incubator-ripple/blob/master/HACKING.md) file.

To get started, you need to setup a few things, first- run (in the project root):

    ./configure

This script will pull down the needed npm packages and initialize the submodules.

## Build Commands

    jake

This will build ripple to the `pkg/` folder. In that folder there are various targets that can be used.

    jake -T

This will describe all the available commands for building and running the tests, etc.

## Running Inside Other Web Browsers

Ripple is (by-design) browser agnostic, and _should_ be able to run inside any web browser.

If you want to run it inside other browsers, you will need to use the `pkg/hosted` target, paired with the CLI's `emulate` command.

Ex (using the NPM package):

    ripple emulate --path to/my/app

    # or

    ripple emulate --remote http://remote-site.com

Then navigating to (your app's html file):

    http://localhost:PORT/index.html?enableripple=true

## CLI & NPM Package

There is a command line interface that can be paired with the client (UI).

It can be used for various things, such as statically hosting an application, and running a local (cross origin) XHR proxy.

To install:

    npm install -g ripple-emulator

This will install a global script called `ripple`. To see usage, run:

    ripple help

## Contributing

The `master` branch is the latest (stable) release. The `next` branch is where all development happens.

If you like the project, and want to contribute code, please issue a pull request (on [GitHub](https://github.com/apache/incubator-ripple/pulls)) into the `next` branch.

Note: You will need to submit an Apache [ICLA](http://www.apache.org/licenses/#clas) (Individual Contributor License Agreement) for your contribution to be accepted.

## Code Guidelines

* 4 spaces per editor tab.
* `jake lint`, no new lint errors introduced.
* All unit tests are green.

## Reference Material &amp; Community

* [Project Site](http://ripple.incubator.apache.org)
