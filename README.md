docker-rtorrent
===============

![Build](https://github.com/ynadji/docker-rtorrent/actions/workflows/docker-image.yml/badge.svg)

A minimal docker container containing the latest version of rtorrent built from
source.

Running
-------

    docker run -it -v /tmp/rtorrent/:/rtorrent ghcr.io/ynadji/rtorrent:latest

Configuring
-----------

In the container, rTorrent is started at the path `/rtorrent` as the rtorrent
user.

To configure the behavior of rtorrent, create a `.rtorrent.rc` file from one of
these guides ([official-guide], [bryanjswift-guide]) and make it available in
the container at the path `/rtorrent/.rtorrent.rc`. Here's an example where the
configuration file is bind mounted from `/tmp/.rtorrent.rc`.

    docker run -it -v /tmp/.rtorrent.rc:/rtorrent/.rtorrent.rc ghcr.io/ynadji/rtorrent:latest

[official-guide]: https://github.com/rakshasa/rtorrent/wiki/Config-Guide
[bryanjswift-guide]: https://gist.github.com/bryanjswift/1525912
