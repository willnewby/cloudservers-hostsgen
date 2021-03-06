# Rackspace Cloud Servers /etc/hosts generator

Auto-populates your /etc/hosts file with the IP addresses (private or public) of Rackspace Cloud Servers on the account specified by the arguments `username` and `apikey`.

### Installation

```
$ sudo pip install git+git://github.com/DavidWittman/cloudservers-hostsgen.git
```

### Usage

```
Usage: cloudservers-hostsgen [options] <username> <apikey>

Auto-generate /etc/hosts entries for Rackspace Cloud Servers

Options:
  -h, --help    show this help message and exit
  -k, --uk      Use London Auth URL (UK accounts only)
  -p, --public  Use Public IP addresses
  -s, --stdout  Output to stdout
```

### Examples
Add servers to /etc/hosts

```
$ sudo cloudservers-hostsgen example_user 1baabb5ca739bedead7d3beef3c8aa3a
Writing new entries to hosts file... Done!
$ cat /etc/hosts
127.0.0.1  localhost

10.180.1.1	example-01
10.180.1.2	example-02
10.182.1.3	example-03
```

Print server list to stdout

```
$ cloudservers-hostsgen -s example_user 1baabb5ca739bedead7d3beef3c8aa3a
10.180.1.1      example-01
10.180.1.2      example-02
10.182.1.3      example-03
```
