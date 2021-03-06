
# loggly-cat

  Stream logs to loggly via stdio.

## Usage

```

  Usage:
    loggly-cat --token t [--tag t]...
    loggly-cat -h | --help
    loggly-cat --version

  Options:
    -t, --token t     loggly api token
    -T, --tag t       loggly tag(s)
    -h, --help        output help information
    -v, --version     output version

```

## Installation

```
$ go get github.com/segmentio/loggly-cat
```

## Examples

  From stdio:

```
$ myapp | loggly-cat -t my-token -T myapp
```

  From tailing:

```
tail -n0 -F /var/log/upstart/buffer.log | loggly-cat -t my-token -T redshift -T red-buffer
```

  From tailing many:

```
tail -n0 -F /var/log/upstart/{buffer,transform,load}.log | loggly-cat -t my-token -T redshift
```

# License

 MIT