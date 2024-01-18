# Pulsar

I'm attempting to bring Juno to the Pulsar-edit, currently a work-in-progress.

# Julia Client

At the moment, this is almost the same (aside from some dependency updates) as the package from [Juno](http://junolab.org), which has switched development to the  [Julia extension for VSCode](https://github.com/julia-vscode/julia-vscode).

This package can be installed in Pulsar-edit directly using the GitHub link, as a drop-in replacement for the JunoLab version of the package (you should reinstall that), after installing the rest of Juno using the [uber-Juno](https://github.com/JunoLab/uber-juno) package. Some of the changes allowed this to install in Pulsar for me, although to get it to actually function I had to navigate to the `~/.pulsar/packages/julia-client/` directory and run `npm ci --no-optional` followed by `npx electron-rebuild -v 12.2.3`. Hoping to fix this at some point...
