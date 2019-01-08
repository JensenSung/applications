[![Build Status](https://travis-ci.org/RIOT-OS/applications.svg?branch=master)](https://travis-ci.org/RIOT-OS/applications)

# RIOT Applications

This repository provides more applications for the [RIOT operating system][riot-repo].
Some of them are just useful tools for development work, others showcase
software provided with RIOT beyond the simple examples [within the RIOT
codebase][riot-repo/examples].

## Usage

To build and use them follow [the instructions in the RIOT repository][getting-started]
and the READMEs within the respective application directory.

The RIOT main code is included as a submodule. This always points to the latest
release. To change the RIOT version to build against (e.g. current master),
clone the RIOT repository in a separate repository and point the `RIOTBASE`
environment variable there:

```sh
# assuming you are in the working directory of your local clone of this repo
cd ..
git clone git@github.com:RIOT-OS/RIOT.git
cd applications
RIOTBASE="../RIOT" BOARD=samr21-xpro make -C sniffer flash
```

Alternatively, you can step into the submodule and check out the current master:

```sh
cd RIOT
git checkout master
git pull
```

Note, that this might lead to build errors, as we do not this repository against
current master.

[riot-repo]: https://github.com/RIOT-OS/RIOT
[riot-repo/examples]: https://github.com/RIOT-OS/RIOT/tree/master/examples
[getting-started]: https://github.com/RIOT-OS/RIOT/blob/master/README.md#getting-started
