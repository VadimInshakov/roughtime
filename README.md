# Roughtime

This package implements a simple Roughtime client based on [Google's
implementation](https://roughtime.googlesource.com/roughtime). To run it, do:
```
$ go get -u github.com/cloudflare/roughtime
$ go install github.com/cloudflare/roughtime...
$ getroughtime -ping roughtime.cloudflare.com:2002 \
    -pubkey gD63hSj3ScS+wuOeGrubXlq35N1c5Lby/S+T7MNTjxo=
ping response: 2018-09-06 19:05:33.054 -0700 PDT ±1s (in 10ms)
```
Or, better yet, use multiple servers!
```
$ getroughtime -config ~/go/src/github.com/cloudflare/roughtime/ecosystem.config
Cloudflare-Roughtime: 2018-09-13 15:46:03.171 -0700 PDT ±1s (in 8ms)
Google-Sandbox-Roughtime: 2018-09-13 15:46:03.213797 -0700 PDT ±1s (in 40ms)
int08h: 2018-09-13 15:46:03.259845 -0700 PDT ±1s (in 61ms)
delta: -18ms
```
For more information about Roughtime and tips for writing your own client, visit
the [developer documentation](https://developers.cloudflare.com/roughtime/).
