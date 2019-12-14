# Pretty Firefox
Pretty Firefox intends to assist on applying custom modifications to Firefox, to versions > 68 .
Since version 68, Firefox application level appearance modifications require changes to be made at css level, not able with legacy addons.

This bash script was created with focus on usability for modifications to Firefox application itself.
There are several projects that were usally applying changes via Firefox addons. Some of these projects moved on providing manual application of their technics, with no automatic way through regular addons.


### Features
Pretty Firefox can:
* be installed as a system package, or used at user account level, with proper installation.
* recognize multiple Firefox profiles and use a selected one
* install a specific package version/release to a selected profile
* download the latest or a specific package version/release
* use (for now) the awesome CustomCSSforFx project, from @Aris-t2 Github user.

We have designed this script to be able to accommodate other alternative scripts/projects, that intend to modify Firefox appearance.

It is developed and tested on Manjaro Linux (Arch based), but it should also work on other Linux systems, perhaps with minor modification. I would appreciate any reports from users of any other distributions, either verifying it works on their system, or reporting bugs and providing info (the files in the temporary working directory), so we try to fix any conflicts, or bugs.

### Requirements
* bash, dos2unix
* wget, git (optional to fetch new versions from web sources)

## Installation (suggested):
```
git clone https://github.com/petsam/prettyfirefox
cd prettyfirefox
chmod +x prettyfirefox
sudo cp prettyfirefox /usr/bin/
sudo mkdir -p /etc/prettyfirefox
sudo cp -r SystemConf/* /etc/prettyfirefox/
```

## Usage
* Run `prettyfirefox --help` to see available options
* Edit package provided configuration files (`.css, .js` etc.), following developers' instructions.
* (Re)start Firefox to see changes

Here is the included help information:

```
prettyfirefox will install, update custom visual modifications to Firefox profile
    using initially CustomCSSforFx repo, potentially adding support for other relevant repos

    Usage:
prettyfirefox [-h][-V|--version][-u|--update][-f|--forceversion][-d|--download][-x|--script][-v|--verbose]
     -h | --help
                     This help information message

     -V | --version
                     Show program version

     -u | --update
                     Update script to the latest version

     -f | --forceversion
                     Update script to a specific version

     -d | --download
                     Download another script version

     -x | --script
                     Firefox profile modification script (i.e. CustomCSSforFx, etc.)

     -v | --verbose
                    Show more detailed information in the output
```