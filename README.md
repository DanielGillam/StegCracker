# StegCracker
[![Build Status](https://travis-ci.org/Paradoxis/StegCracker.svg?branch=master)](https://travis-ci.org/Paradoxis/StegCracker)
[![PyPI version](https://badge.fury.io/py/stegcracker.svg)](https://badge.fury.io/py/stegcracker)
[![codecov](https://codecov.io/gh/Paradoxis/StegCracker/branch/master/graph/badge.svg)](https://codecov.io/gh/Paradoxis/StegCracker)

Steganography brute-force utility to uncover hidden data inside files.

## Usage
Using stegcracker is simple, pass a file to it as it's first parameter and 
optionally pass the path to a wordlist of passwords to try as it's second 
parameter. If you don't specify the wordlist, the tool will try to use the 
built-in rockyou.txt wordlist which ships with Kali Linux. If you are running a 
different distribution, you can download the rockyou wordlist 
[here](https://github.com/danielmiessler/SecLists/raw/master/Passwords/Leaked-Databases/rockyou.txt.tar.gz).

```
$ stegcracker <file> [<wordlist>]
```

## Requirements
The program requires Python 3.6 and the steghide binary to be installed. If 
python 3.6 is not installed, check out [this](https://unix.stackexchange.com/questions/332641/how-to-install-python-3-6)
guide on how to do so, and steghide can be installed by using the following command:

```
$ sudo apt-get install steghide -y
```

## Installation
To install the program, run the following command:

```
$ pip3.6 install stegcracker
```

## Updating
To update the program, simply pass `-U` to the installation command:

```
$ pip3.6 install stegcracker -U --force-reinstall
```

## Example

![demo](https://github.com/Paradoxis/StegCracker/raw/master/stegcracker.gif)

## Upgrading from 1.X
If you're upgrading StegCracker from the original 1.X release, please remove the existing version first:

```
$ sudo rm --force $(which stegcracker)
```

## Looking for the old version?
While I reccomended using the latest and greatest version, you might want to install the older version of StegCracker (you might not be able to install Python 3.6 on your platform, or you're just feeling nostalgic, I don't blame you). You can download it from the [v1.0.0 tag](https://github.com/Paradoxis/StegCracker/blob/v1.0.0/stegcracker) _(note: all issues or pull requests regarding this version will be be ignored)_.

## License
Copyright 2019 - Luke Paris (Paradoxis)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, 
including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to 
do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND 
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF 
OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
