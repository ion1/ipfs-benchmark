# ipfs-benchmark

A quick and dirty pair of scripts to benchmark the bitswap overhead in [IPFS](https://ipfs.io/).

* Install [go-ipfs](https://ipfs.io/docs/install/), [rrdtool](http://oss.oetiker.ch/rrdtool/), [curl](http://curl.haxx.se/) and [jq](https://stedolan.github.io/jq/).
* Run `ipfs daemon`.
* Change to a new temporary directory and run `ipfs-collect`. It will create `ipfs.rrd` and add measurements to it periodically.
* Run `ipfs get -o data <hash>` in the same directory to download a large file.
* Run `ipfs-graph` to generate `ipfs.png` from `ipfs.rrd`.
