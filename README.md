Manages persistant backups for mobile devices like laptops and cell phones that cannot be realiably backed up on a set schedule.

REQUIREMENTS
============
- *nix based operating system (only tested on linux)
- ping and rsync installed


INSTALL
======
- Add the hosts to be backed up to the targets.py file
- Add rsa keys to the remote hosts to allow for passwordless login
- Manually select yes when you connect to a new host

PERSISTANT BACKUPS
==================
- Use cron to call the daily backup (persisant -d) once a day
- Use cron to call the persist backup (persistant -p) every 10 minutes

USAGE
=====
```
usage: persistant [-h] [-d] [-p] [-i] [-v] [-t] [--ping PING_PATH]
                  [--rsync RSYNC_PATH]

Backup remote files.

optional arguments:
  -h, --help          show this help message and exit
  -d, --daily         creates a new daily backup
  -p, --persist       tries to perform missed backups
  -i, --incremental   performs an incremental backup instead of a new backup
  -v, --verbose       explains what is being done
  -t, --test          runs rsync in test mode
  --ping PING_PATH    specify a path for ping, default:"/bin/ping"
  --rsync RSYNC_PATH  specify a path for rsync, default:"/usr/bin/rsync"
```

TODO
====
- support for archiving directories
- support for deleting old backups

LICENSE
=======
```
Copyright (c) 2013 Ben Doan

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```
[![githalytics.com alpha](https://cruel-carlota.pagodabox.com/869c0d7a59ff58eee47032547b43d8fa "githalytics.com")](http://githalytics.com/BenDoan/persistant-backup)
