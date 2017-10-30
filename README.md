# Simple SYN Flooder and Spoofer
This was created for educational purposes to demonstrate how [SYN attacks] work. It can also be used to test the effectiveness of firewalls claiming to block SYN flooding.

### Install
pip install -r requirements.txt

### Usage
```
Usage:
  syn_flooder.py <dst_ip> <dst_port> [--sleep=<sec>] [-v] [-vv]

  Options:
    -h, --help            Show this screen.
    --version             Show version.
    --sleep=<sec>         How many seconds to sleep betseen scans [default: 0].
    -v, --verbose         Show addresses being spoofed.
    -vv, --very-verbose   Display everything.
```

[SYN attacks]: <https://en.wikipedia.org/wiki/SYN_flood>
