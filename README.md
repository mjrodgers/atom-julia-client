# Pulsar

I'm attempting to bring Juno to the Pulsar-edit, currently a work-in-progress.

# Julia Client

At the moment, this is almost the same (aside from some dependency updates) as the package from [Juno](http://junolab.org), which has switched development to the  [Julia extension for VSCode](https://github.com/julia-vscode/julia-vscode).

This package can be installed in Pulsar-edit directly using the GitHub link, and is a drop-in replacement for the JunoLab version of the package, after installing the rest of Juno using the [uber-Juno](https://github.com/JunoLab/uber-juno) package. With the following caveats:

There are now a few obstacles to getting this set up properly in Pulsar.
- NOTE: There are compatibility problems with Julia 1.11, but it works well with 1.10.
- Firstly, the `uber-juno` package should be installed from the above GitHub link, since there are some bugs that have been fixed since the last time the Atom/Pulsar package was updated.
- the `uber-juno` package will install all the relevant packages, but still won't work. So you will have to uninstall the [`ink`](https://github.com/JunoLab/atom-ink)  and [`julia-client`](https://github.com/mjrodgers/atom-julia-client) packages it installs, and reinstall from their GitHub links (with `atom-client` using this modified version).

Finally, it is possible that you may have to navigate to the `~/.pulsar/packages/julia-client/` directory and run `npm ci --no-optional` followed by `npx electron-rebuild -v 12.2.3`. I think this is fixed in recent versions of Pulsar.
