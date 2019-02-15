# Simple SYN Flooder and Spoofer
This was created for educational purposes to demonstrate how [SYN attacks] work. It can also be used to test the effectiveness of firewalls claiming to block SYN flooding.

## Multiprocessing version
![multi_syn.py](multi_syn.py) uses multiprocessing, meaning it will create *N* workers which will run their own spoofer and SYN flooding. Specify `--workers=N` to control how many processes you want to spawn.

The spoof addresses are hardcoded and will use following format `10.10.n` where *n* is a process number. For example, if you spawn 4 workers, the spoof address per worker becomes:

```
10.10.1.x
10.10.2.x
10.10.3.x
10.10.4.x
```

## Install
Tested and developed with Python3.6.

You man need to change line ending characters for DOS.

`sudo apt install python3-pip`

`pip3 install -r requirements.txt`

## Usage
You may need to run the program as root.
<src_net> assumes /24 network.

```
Usage:
  syn_flooder.py <dst_ip> <dst_port> <src_net> [--sleep=<sec>] [--verbose] [--very-verbose]

Options:
  -h, --help            Show this screen.
  --version             Show version.
  --sleep=<seconds>     How many seconds to sleep between scans [default: 0].
  --verbose             Show addresses being spoofed. [default: False]
  --very-verbose        Display everything. [default: False]
```

[SYN attacks]: <https://en.wikipedia.org/wiki/SYN_flood>
