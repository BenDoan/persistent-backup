Manages persistant backups for mobile devices like laptops and cell phones that cannot be realiably backed up on a set schedule.

REQUIREMENTS
============
- *nix based operating system
- ping installed at '/bin/ping'
- RSync installed at '/usr/bin/rsync'

INSTALL
======
- Add the hosts to be backed up to the targets.py file
- Add rsa keys to the remote hosts to allow passwordless login
- Manually select yes when you connect to a new host

USAGE
=====
```
usage: persistant [-h] [-d] [-p] [-i] [-v]

Backup remote files.

optional arguments:
  -h, --help         show this help message and exit
  -d, --daily        creates a new daily backup
  -p, --persist      tries to perform missed backups
  -i, --incremental  performs an incremental backup instead of a new backup
  -v, --verbose      explains what is being done
```

LICENSE
=======
```
Copyright (c) 2013 Ben Doan

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```
