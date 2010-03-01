# npm – The Node Package Manager

npm is a little package manager for the Node javascript library.

For now, this README is more of a task list/roadmap than a proper "how to use this" type doc.

## Contributing

If you're interested in helping, that's awesome!  Please fork this project, implement some of the things on the list, and then let me know.  You can usually find me in #node.js on freenode.net, or you can reach me via <i@izs.me>.

## Installation

To install npm, do this:

    $ node install-npm.js

That will use npm to install itself, like [Ouroboros](http://en.wikipedia.org/wiki/Ouroboros).  From there, you can call the command line program which is cleverly named `npm`.

## What works now:

In a nodejs program:

    require("./npm").install(tarball)

on the command line:

    npm install <tarball>

This installs the package, where `tarball` is a url or path to a `.tgz` file that contains a package with a `package.json` file in the root.

This'll create some stuff in `$HOME/.node_libraries`.  It supports installing multiple versions of the same thing.  Version activation, dependency resolution, and registry awareness are planned next.


## Todo

* Install packages from the registry
* Install missing dependencies.  This, with the registry, will make it so that circular dependencies are supported.
* Safely uninstall packages, failing if anything depends on it.
* Keep track of what depends on what.
* Add an "activate" step.  Now that the deps are all included into the package, this isn't any big deal, really.  But the list command should show which one is active.
