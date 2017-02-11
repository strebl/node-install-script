# Easy Install node.js

Automated node.js installers for OS X and Ubuntu

## Installation

```bash
# install node.js
curl -fsSL bit.ly/nodejs-installer | bash

# using wget instead of curl (Ubuntu)
wget -nv bit.ly/nodejs-installer -O - | bash
```

## Choosing a specific version

```bash
echo "Current node.js version is $(curl -fsL https://nodejs.org/dist/index.tab | head -2 | tail -1 | cut -f 1)"
```

```bash
# To install a specific version rather than defaulting to latest
echo "v7.5.0" > /tmp/NODE_VER
```

## Notes

* [OS X](#apple-os-x)
* [Ubuntu Linux](#ubuntu-linux)
* [Important Notes](#other-things-you-should-know)

### Apple OS X

First you need to **Install XCode Command Line Tools**

```bash
xcode-select --install
```

Then you need to **Accept the XCode License** by running any command installed by Xcode with sudo. We'll use git.

```bash
sudo git --version
```

You can scroll to the bottom by hitting shift+G (capital G).

Type `agree` and hit enter to accept the license.

Now you can install node.js

```bash
curl -fsSL bit.ly/nodejs-installer -o /tmp/node-dev.sh; bash /tmp/node-dev.sh
```

*TODO*: Make it easier to accepting the license (automatic?)

### Ubuntu Linux

```bash
wget -nv bit.ly/nodejs-installer -O /tmp/node-dev.sh; bash /tmp/node-dev.sh
```
